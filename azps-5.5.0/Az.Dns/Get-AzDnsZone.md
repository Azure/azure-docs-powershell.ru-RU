---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237936"
---
# <span data-ttu-id="12e98-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e98-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="12e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e98-102">SYNOPSIS</span></span>
<span data-ttu-id="12e98-103">Получает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="12e98-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="12e98-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12e98-104">SYNTAX</span></span>

### <span data-ttu-id="12e98-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12e98-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e98-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12e98-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e98-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e98-107">DESCRIPTION</span></span>
<span data-ttu-id="12e98-108">**Cmdlet Get-AzDnsZone** получает зону службы доменных имен (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e98-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="12e98-109">Если задать параметр *Name,* возвращается один **объект DnsZone.**</span><span class="sxs-lookup"><span data-stu-id="12e98-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="12e98-110">Если параметр Name  не задан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e98-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="12e98-111">Для обновления зоны можно использовать объект **DnsZone,** например **объекты RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="12e98-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="12e98-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12e98-112">EXAMPLES</span></span>

### <span data-ttu-id="12e98-113">Пример 1. Получить зону</span><span class="sxs-lookup"><span data-stu-id="12e98-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="12e98-114">В этом примере зона DNS myzone.com из указанной группы ресурсов, а затем хранится в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="12e98-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="12e98-115">Пример 2. Получить все зоны в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="12e98-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="12e98-116">В этом примере все зоны DNS в указанной группе ресурсов, а затем в переменной $Zones ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e98-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="12e98-117">Пример 3. Получить все зоны подписки</span><span class="sxs-lookup"><span data-stu-id="12e98-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="12e98-118">В этом примере все зоны DNS в текущей подписке Azure, а затем в переменной $Zones Azure.</span><span class="sxs-lookup"><span data-stu-id="12e98-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="12e98-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e98-119">PARAMETERS</span></span>

### <span data-ttu-id="12e98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e98-120">-DefaultProfile</span></span>
<span data-ttu-id="12e98-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="12e98-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e98-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12e98-122">-Name</span></span>
<span data-ttu-id="12e98-123">Указывает имя зоны DNS, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="12e98-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="12e98-124">Если значение параметра *Name* не задано, этот cmdlet получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e98-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="12e98-125">Если параметр *ResourceGroupName не* задан, этот cmdlet получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="12e98-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="12e98-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e98-126">-ResourceGroupName</span></span>
<span data-ttu-id="12e98-127">Имя группы ресурсов, которая содержит зону DNS, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="12e98-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="12e98-128">Если параметр *ResourceGroupName* не указан, необходимо также опустить параметр *Name.*</span><span class="sxs-lookup"><span data-stu-id="12e98-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="12e98-129">В этом случае этот cmdlet получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="12e98-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="12e98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e98-130">CommonParameters</span></span>
<span data-ttu-id="12e98-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e98-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e98-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e98-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12e98-133">INPUTS</span></span>

### <span data-ttu-id="12e98-134">System.String</span><span class="sxs-lookup"><span data-stu-id="12e98-134">System.String</span></span>

## <span data-ttu-id="12e98-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12e98-135">OUTPUTS</span></span>

### <span data-ttu-id="12e98-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="12e98-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="12e98-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12e98-137">NOTES</span></span>

## <span data-ttu-id="12e98-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12e98-138">RELATED LINKS</span></span>

[<span data-ttu-id="12e98-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e98-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="12e98-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e98-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="12e98-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e98-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
