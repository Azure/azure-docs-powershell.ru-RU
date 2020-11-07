---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: c52c9e743555c0c66afa8cc72343215a0888a7c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733164"
---
# <span data-ttu-id="b2019-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2019-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="b2019-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2019-102">SYNOPSIS</span></span>
<span data-ttu-id="b2019-103">Возвращает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="b2019-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2019-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2019-104">SYNTAX</span></span>

### <span data-ttu-id="b2019-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2019-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2019-106">Группа</span><span class="sxs-lookup"><span data-stu-id="b2019-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2019-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2019-107">DESCRIPTION</span></span>
<span data-ttu-id="b2019-108">Командлет **Get-AzureRmDnsZone** получает DNS-зону из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2019-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="b2019-109">Если указан параметр *Name* , возвращается один объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="b2019-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="b2019-110">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2019-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="b2019-111">Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b2019-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="b2019-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2019-112">EXAMPLES</span></span>

### <span data-ttu-id="b2019-113">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="b2019-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="b2019-114">В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="b2019-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="b2019-115">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2019-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b2019-116">В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="b2019-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="b2019-117">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="b2019-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="b2019-118">В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="b2019-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="b2019-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2019-119">PARAMETERS</span></span>

### <span data-ttu-id="b2019-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2019-120">-DefaultProfile</span></span>
<span data-ttu-id="b2019-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2019-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2019-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2019-122">-Name</span></span>
<span data-ttu-id="b2019-123">Указывает имя зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b2019-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="b2019-124">Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2019-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="b2019-125">Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b2019-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b2019-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2019-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2019-127">Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b2019-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="b2019-128">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="b2019-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="b2019-129">В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b2019-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b2019-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2019-130">CommonParameters</span></span>
<span data-ttu-id="b2019-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2019-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2019-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2019-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2019-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2019-133">INPUTS</span></span>

### <span data-ttu-id="b2019-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2019-134">System.String</span></span>

## <span data-ttu-id="b2019-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2019-135">OUTPUTS</span></span>

### <span data-ttu-id="b2019-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b2019-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b2019-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2019-137">NOTES</span></span>

## <span data-ttu-id="b2019-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2019-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2019-139">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2019-139">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="b2019-140">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2019-140">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="b2019-141">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b2019-141">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
