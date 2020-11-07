---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912314"
---
# <span data-ttu-id="f7988-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f7988-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="f7988-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7988-102">SYNOPSIS</span></span>
<span data-ttu-id="f7988-103">Получение частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="f7988-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="f7988-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7988-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7988-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7988-105">DESCRIPTION</span></span>
<span data-ttu-id="f7988-106">Командлет **Get-AzPrivateDnsZone** получает зону DNS частной системы доменных имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7988-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="f7988-107">Если указан параметр *Name* , возвращается один объект **PrivateDnsZone** .</span><span class="sxs-lookup"><span data-stu-id="f7988-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="f7988-108">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7988-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="f7988-109">Вы можете использовать объект **PrivateDnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f7988-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="f7988-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7988-110">EXAMPLES</span></span>

### <span data-ttu-id="f7988-111">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="f7988-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="f7988-112">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f7988-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="f7988-113">Этот пример возвращает все закрытые зоны DNS в заданной группе ресурсов, а затем сохраняет их в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="f7988-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="f7988-114">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="f7988-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="f7988-115">В этом примере выполняется получение всех закрытых зон DNS в текущей подписке Azure, а затем они сохраняются в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="f7988-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="f7988-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7988-116">PARAMETERS</span></span>

### <span data-ttu-id="f7988-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7988-117">-DefaultProfile</span></span>
<span data-ttu-id="f7988-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7988-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7988-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7988-119">-Name</span></span>
<span data-ttu-id="f7988-120">Указывает имя частной зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f7988-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="f7988-121">Если вы не укажете значение параметра *Name* , этот командлет будет получать все закрытые зоны DNS в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7988-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="f7988-122">Если параметр *ResourceGroupName* также опущен, этот командлет получает все закрытые зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7988-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="f7988-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7988-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7988-124">Указывает имя группы ресурсов, содержащей частную зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f7988-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="f7988-125">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="f7988-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="f7988-126">В этом случае этот командлет получает все закрытые зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7988-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="f7988-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7988-127">CommonParameters</span></span>
<span data-ttu-id="f7988-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7988-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7988-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7988-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7988-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7988-130">INPUTS</span></span>

### <span data-ttu-id="f7988-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7988-131">None</span></span>

## <span data-ttu-id="f7988-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7988-132">OUTPUTS</span></span>

### <span data-ttu-id="f7988-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f7988-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="f7988-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7988-134">NOTES</span></span>

## <span data-ttu-id="f7988-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7988-135">RELATED LINKS</span></span>

[<span data-ttu-id="f7988-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f7988-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="f7988-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f7988-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="f7988-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f7988-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
