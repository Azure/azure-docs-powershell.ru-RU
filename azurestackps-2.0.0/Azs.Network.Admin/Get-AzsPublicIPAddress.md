---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910490"
---
# <span data-ttu-id="b5ed8-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5ed8-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="b5ed8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ed8-103">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-103">List of public ip addresses.</span></span>

## <span data-ttu-id="b5ed8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5ed8-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5ed8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ed8-106">Список общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-106">List of public ip addresses.</span></span>

## <span data-ttu-id="b5ed8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ed8-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5ed8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="b5ed8-109">Получение списка общедоступных IP-адресов, выделенных или не выделенных.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="b5ed8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ed8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ed8-111">-DefaultProfile</span></span>
<span data-ttu-id="b5ed8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ed8-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b5ed8-113">-Filter</span></span>
<span data-ttu-id="b5ed8-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="b5ed8-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b5ed8-115">-InlineCount</span></span>
<span data-ttu-id="b5ed8-116">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b5ed8-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b5ed8-117">-OrderBy</span></span>
<span data-ttu-id="b5ed8-118">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b5ed8-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="b5ed8-119">-Skip</span></span>
<span data-ttu-id="b5ed8-120">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="b5ed8-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5ed8-121">-SubscriptionId</span></span>
<span data-ttu-id="b5ed8-122">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5ed8-123">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5ed8-124">-Top</span><span class="sxs-lookup"><span data-stu-id="b5ed8-124">-Top</span></span>
<span data-ttu-id="b5ed8-125">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-125">OData top parameter.</span></span>

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

### <span data-ttu-id="b5ed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ed8-126">CommonParameters</span></span>
<span data-ttu-id="b5ed8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5ed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ed8-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5ed8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ed8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5ed8-129">INPUTS</span></span>

## <span data-ttu-id="b5ed8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ed8-130">OUTPUTS</span></span>

### <span data-ttu-id="b5ed8-131">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5ed8-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="b5ed8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5ed8-132">NOTES</span></span>

## <span data-ttu-id="b5ed8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5ed8-133">RELATED LINKS</span></span>

