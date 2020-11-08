---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079642"
---
# <span data-ttu-id="c8a5a-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c8a5a-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="c8a5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a5a-103">Возвращает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="c8a5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8a5a-104">SYNTAX</span></span>

### <span data-ttu-id="c8a5a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8a5a-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a5a-106">Группа</span><span class="sxs-lookup"><span data-stu-id="c8a5a-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a5a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8a5a-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a5a-108">Командлет **Get-AzDnsZone** получает DNS-зону из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="c8a5a-109">Если указан параметр *Name* , возвращается один объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="c8a5a-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="c8a5a-110">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="c8a5a-111">Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c8a5a-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="c8a5a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8a5a-112">EXAMPLES</span></span>

### <span data-ttu-id="c8a5a-113">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="c8a5a-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="c8a5a-114">В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="c8a5a-115">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8a5a-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c8a5a-116">В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="c8a5a-117">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="c8a5a-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="c8a5a-118">В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="c8a5a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8a5a-119">PARAMETERS</span></span>

### <span data-ttu-id="c8a5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a5a-120">-DefaultProfile</span></span>
<span data-ttu-id="c8a5a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8a5a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a5a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8a5a-122">-Name</span></span>
<span data-ttu-id="c8a5a-123">Указывает имя зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="c8a5a-124">Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="c8a5a-125">Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8a5a-127">Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="c8a5a-128">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="c8a5a-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="c8a5a-129">В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a5a-130">CommonParameters</span></span>
<span data-ttu-id="c8a5a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8a5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a5a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a5a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a5a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8a5a-133">INPUTS</span></span>

### <span data-ttu-id="c8a5a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a5a-134">System.String</span></span>

## <span data-ttu-id="c8a5a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8a5a-135">OUTPUTS</span></span>

### <span data-ttu-id="c8a5a-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="c8a5a-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="c8a5a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8a5a-137">NOTES</span></span>

## <span data-ttu-id="c8a5a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8a5a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8a5a-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c8a5a-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="c8a5a-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c8a5a-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="c8a5a-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="c8a5a-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
