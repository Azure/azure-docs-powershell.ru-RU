---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506764"
---
# <span data-ttu-id="b95c7-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b95c7-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="b95c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b95c7-103">Возвращает частную зону DNS.</span><span class="sxs-lookup"><span data-stu-id="b95c7-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="b95c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b95c7-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b95c7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b95c7-105">DESCRIPTION</span></span>
<span data-ttu-id="b95c7-106">Чтобы получить зону личных доменных имен (DNS) из указанной группы ресурсов, можно получить зону личных доменных имен **(Get-AzPrivateDnsZone).**</span><span class="sxs-lookup"><span data-stu-id="b95c7-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="b95c7-107">Если задать параметр *Name,* возвращается один объект **PrivateDnsZone.**</span><span class="sxs-lookup"><span data-stu-id="b95c7-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="b95c7-108">Если не указать параметр *Name,* возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b95c7-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="b95c7-109">Объект **PrivateDnsZone** можно использовать для обновления зоны (например, чтобы добавить в нее **объекты RecordSet).**</span><span class="sxs-lookup"><span data-stu-id="b95c7-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="b95c7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b95c7-110">EXAMPLES</span></span>

### <span data-ttu-id="b95c7-111">Пример 1. Получить зону</span><span class="sxs-lookup"><span data-stu-id="b95c7-111">Example 1: Get a zone</span></span>
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

### <span data-ttu-id="b95c7-112">Пример 2. Получить все зоны в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b95c7-112">Example 2: Get all of the zones in a resource group</span></span>
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

<span data-ttu-id="b95c7-113">В этом примере все зоны Private DNS в указанной группе ресурсов, а затем в переменной $Zones ресурса.</span><span class="sxs-lookup"><span data-stu-id="b95c7-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="b95c7-114">Пример 3. Получить все зоны подписки</span><span class="sxs-lookup"><span data-stu-id="b95c7-114">Example 3: Get all of the zones in a subscription</span></span>
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

<span data-ttu-id="b95c7-115">В этом примере все зоны частных DNS в текущей подписке Azure, а затем в переменной $Zones Azure.</span><span class="sxs-lookup"><span data-stu-id="b95c7-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="b95c7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95c7-116">PARAMETERS</span></span>

### <span data-ttu-id="b95c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95c7-117">-DefaultProfile</span></span>
<span data-ttu-id="b95c7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b95c7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b95c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b95c7-119">-Name</span></span>
<span data-ttu-id="b95c7-120">Указывает имя зоны private DNS, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="b95c7-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="b95c7-121">Если значение параметра *Name* не задано, этот cmdlet возвращает все зоны Private DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b95c7-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="b95c7-122">Если параметр *ResourceGroupName не* задан, этот cmdlet получает все зоны частных DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b95c7-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b95c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b95c7-124">Имя группы ресурсов, которая содержит частную зону DNS, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b95c7-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="b95c7-125">Если параметр *ResourceGroupName* не указан, необходимо также опустить параметр *Name.*</span><span class="sxs-lookup"><span data-stu-id="b95c7-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="b95c7-126">В этом случае этот cmdlet получает все зоны частных DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="b95c7-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="b95c7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95c7-127">CommonParameters</span></span>
<span data-ttu-id="b95c7-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95c7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95c7-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95c7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95c7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b95c7-130">INPUTS</span></span>

### <span data-ttu-id="b95c7-131">Нет</span><span class="sxs-lookup"><span data-stu-id="b95c7-131">None</span></span>

## <span data-ttu-id="b95c7-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b95c7-132">OUTPUTS</span></span>

### <span data-ttu-id="b95c7-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b95c7-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b95c7-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b95c7-134">NOTES</span></span>

## <span data-ttu-id="b95c7-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b95c7-135">RELATED LINKS</span></span>

[<span data-ttu-id="b95c7-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b95c7-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="b95c7-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b95c7-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="b95c7-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b95c7-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)