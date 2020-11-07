---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733282"
---
# <span data-ttu-id="604eb-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="604eb-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="604eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="604eb-102">SYNOPSIS</span></span>
<span data-ttu-id="604eb-103">Возвращает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="604eb-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="604eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="604eb-104">SYNTAX</span></span>

### <span data-ttu-id="604eb-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="604eb-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="604eb-106">Группа</span><span class="sxs-lookup"><span data-stu-id="604eb-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="604eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="604eb-107">DESCRIPTION</span></span>
<span data-ttu-id="604eb-108">Командлет **Get-AzureRmDnsZone** получает DNS-зону из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="604eb-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="604eb-109">Если указан параметр *Name* , возвращается один объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="604eb-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="604eb-110">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="604eb-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="604eb-111">Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="604eb-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="604eb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="604eb-112">EXAMPLES</span></span>

### <span data-ttu-id="604eb-113">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="604eb-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="604eb-114">В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="604eb-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="604eb-115">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="604eb-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="604eb-116">В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="604eb-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="604eb-117">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="604eb-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="604eb-118">В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="604eb-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="604eb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="604eb-119">PARAMETERS</span></span>

### <span data-ttu-id="604eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604eb-120">-DefaultProfile</span></span>
<span data-ttu-id="604eb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="604eb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604eb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="604eb-122">-Name</span></span>
<span data-ttu-id="604eb-123">Указывает имя зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="604eb-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="604eb-124">Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="604eb-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="604eb-125">Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="604eb-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="604eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="604eb-127">Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="604eb-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="604eb-128">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="604eb-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="604eb-129">В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="604eb-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="604eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604eb-130">CommonParameters</span></span>
<span data-ttu-id="604eb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="604eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604eb-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604eb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604eb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="604eb-133">INPUTS</span></span>

### <span data-ttu-id="604eb-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="604eb-134">None</span></span>
<span data-ttu-id="604eb-135">Этот командлет не позволяет передавать входные данные.</span><span class="sxs-lookup"><span data-stu-id="604eb-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="604eb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="604eb-136">OUTPUTS</span></span>

### <span data-ttu-id="604eb-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="604eb-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="604eb-138">Этот командлет возвращает объект, который представляет зону DNS.</span><span class="sxs-lookup"><span data-stu-id="604eb-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="604eb-139">Если имя зоны не задано, возвращается массив объектов зоны.</span><span class="sxs-lookup"><span data-stu-id="604eb-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="604eb-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="604eb-140">NOTES</span></span>

## <span data-ttu-id="604eb-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="604eb-141">RELATED LINKS</span></span>

[<span data-ttu-id="604eb-142">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="604eb-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="604eb-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="604eb-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="604eb-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="604eb-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
