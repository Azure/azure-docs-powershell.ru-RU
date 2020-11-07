---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914486"
---
# <span data-ttu-id="2fcc9-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fcc9-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="2fcc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcc9-103">Возвращает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fcc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fcc9-104">SYNTAX</span></span>

### <span data-ttu-id="2fcc9-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fcc9-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="2fcc9-106">Группа</span><span class="sxs-lookup"><span data-stu-id="2fcc9-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="2fcc9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fcc9-107">DESCRIPTION</span></span>
<span data-ttu-id="2fcc9-108">Командлет **Get-AzureRmDnsZone** получает DNS-зону из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="2fcc9-109">Если указан параметр *Name* , возвращается один объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="2fcc9-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="2fcc9-110">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="2fcc9-111">Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="2fcc9-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="2fcc9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fcc9-112">EXAMPLES</span></span>

### <span data-ttu-id="2fcc9-113">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="2fcc9-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="2fcc9-114">В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2fcc9-115">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="2fcc9-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2fcc9-116">В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="2fcc9-117">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="2fcc9-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="2fcc9-118">В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="2fcc9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fcc9-119">PARAMETERS</span></span>

### <span data-ttu-id="2fcc9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fcc9-120">-Name</span></span>
<span data-ttu-id="2fcc9-121">Указывает имя зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="2fcc9-122">Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="2fcc9-123">Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcc9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fcc9-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fcc9-125">Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="2fcc9-126">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="2fcc9-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="2fcc9-127">В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcc9-128">CommonParameters</span></span>
<span data-ttu-id="2fcc9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcc9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fcc9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcc9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fcc9-131">INPUTS</span></span>

### <span data-ttu-id="2fcc9-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="2fcc9-132">None</span></span>
<span data-ttu-id="2fcc9-133">Этот командлет не позволяет передавать входные данные.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="2fcc9-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fcc9-134">OUTPUTS</span></span>

### <span data-ttu-id="2fcc9-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2fcc9-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2fcc9-136">Этот командлет возвращает объект, который представляет зону DNS.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="2fcc9-137">Если имя зоны не задано, возвращается массив объектов зоны.</span><span class="sxs-lookup"><span data-stu-id="2fcc9-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="2fcc9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fcc9-138">NOTES</span></span>

## <span data-ttu-id="2fcc9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fcc9-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fcc9-140">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fcc9-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="2fcc9-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fcc9-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="2fcc9-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fcc9-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
