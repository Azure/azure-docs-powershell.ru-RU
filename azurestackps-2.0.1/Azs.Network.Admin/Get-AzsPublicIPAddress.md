---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075204"
---
# <span data-ttu-id="c909b-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c909b-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="c909b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c909b-102">SYNOPSIS</span></span>
<span data-ttu-id="c909b-103">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c909b-103">List of public ip addresses.</span></span>

## <span data-ttu-id="c909b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c909b-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c909b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c909b-105">DESCRIPTION</span></span>
<span data-ttu-id="c909b-106">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c909b-106">List of public ip addresses.</span></span>

## <span data-ttu-id="c909b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c909b-107">EXAMPLES</span></span>

### <span data-ttu-id="c909b-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c909b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="c909b-109">Получение списка общедоступных IP-адресов, выделенных или не выделенных.</span><span class="sxs-lookup"><span data-stu-id="c909b-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="c909b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c909b-110">PARAMETERS</span></span>

### <span data-ttu-id="c909b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c909b-111">-DefaultProfile</span></span>
<span data-ttu-id="c909b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c909b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c909b-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="c909b-113">-Filter</span></span>
<span data-ttu-id="c909b-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c909b-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="c909b-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="c909b-115">-InlineCount</span></span>
<span data-ttu-id="c909b-116">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="c909b-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="c909b-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c909b-117">-OrderBy</span></span>
<span data-ttu-id="c909b-118">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="c909b-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="c909b-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="c909b-119">-Skip</span></span>
<span data-ttu-id="c909b-120">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="c909b-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="c909b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c909b-121">-SubscriptionId</span></span>
<span data-ttu-id="c909b-122">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c909b-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c909b-123">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c909b-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c909b-124">-Top</span><span class="sxs-lookup"><span data-stu-id="c909b-124">-Top</span></span>
<span data-ttu-id="c909b-125">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="c909b-125">OData top parameter.</span></span>

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

### <span data-ttu-id="c909b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c909b-126">CommonParameters</span></span>
<span data-ttu-id="c909b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c909b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c909b-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c909b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c909b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c909b-129">INPUTS</span></span>

## <span data-ttu-id="c909b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c909b-130">OUTPUTS</span></span>

### <span data-ttu-id="c909b-131">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="c909b-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="c909b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c909b-132">NOTES</span></span>

## <span data-ttu-id="c909b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c909b-133">RELATED LINKS</span></span>

