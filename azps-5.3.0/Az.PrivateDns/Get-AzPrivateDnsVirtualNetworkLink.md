---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506766"
---
# <span data-ttu-id="05550-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="05550-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="05550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05550-102">SYNOPSIS</span></span>
<span data-ttu-id="05550-103">Получает виртуальную сетевую ссылку, связанную с указанной частной зоной DNS.</span><span class="sxs-lookup"><span data-stu-id="05550-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="05550-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05550-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05550-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05550-105">DESCRIPTION</span></span>
<span data-ttu-id="05550-106">Командлет **Get-AzPrivateDnsVirtualNetworkLink** получает виртуальные сетевые ссылки, связанные с определенной частной зоной DNS из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05550-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="05550-107">Если указать параметр *Name,* возвращается один **объект PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="05550-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="05550-108">Если параметр Name  не задан, возвращается массив, содержащий все связи, связанные с зоной в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05550-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="05550-109">Для обновления ссылки можно использовать объект **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="05550-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="05550-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05550-110">EXAMPLES</span></span>

### <span data-ttu-id="05550-111">Пример 1. Получите виртуальную сетевую связь.</span><span class="sxs-lookup"><span data-stu-id="05550-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="05550-112">В этом примере получается моя ссылка виртуальной сети, связанная с частной зоной DNS myzone.com из указанной группы ресурсов, и она сохраняется в переменной $Link ресурса.</span><span class="sxs-lookup"><span data-stu-id="05550-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="05550-113">Пример 2. Получить все связи, связанные с зоной в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05550-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="05550-114">В этом примере все виртуальные сетевые связи, связанные с частной зоной DNS "myzone.com", в указанной группе ресурсов, а затем $Links переменной.</span><span class="sxs-lookup"><span data-stu-id="05550-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="05550-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05550-115">PARAMETERS</span></span>

### <span data-ttu-id="05550-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05550-116">-DefaultProfile</span></span>
<span data-ttu-id="05550-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05550-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05550-118">-Name</span><span class="sxs-lookup"><span data-stu-id="05550-118">-Name</span></span>
<span data-ttu-id="05550-119">Указывает имя виртуальной сетевой ссылки, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="05550-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="05550-120">Если значение параметра *Name* не задано, этот cmdlet получает все связи, связанные с указанной закрытой зоной DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05550-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="05550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05550-121">-ResourceGroupName</span></span>
<span data-ttu-id="05550-122">Имя группы ресурсов, которая содержит виртуальную сетевую ссылку, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="05550-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05550-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="05550-123">-ZoneName</span></span>
<span data-ttu-id="05550-124">Указывает имя зоны частных DNS, с которую связана виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="05550-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05550-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05550-125">CommonParameters</span></span>
<span data-ttu-id="05550-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05550-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05550-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05550-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05550-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05550-128">INPUTS</span></span>

### <span data-ttu-id="05550-129">Нет</span><span class="sxs-lookup"><span data-stu-id="05550-129">None</span></span>

## <span data-ttu-id="05550-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05550-130">OUTPUTS</span></span>

### <span data-ttu-id="05550-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="05550-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="05550-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05550-132">NOTES</span></span>

## <span data-ttu-id="05550-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05550-133">RELATED LINKS</span></span>

[<span data-ttu-id="05550-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="05550-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="05550-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="05550-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="05550-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="05550-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
