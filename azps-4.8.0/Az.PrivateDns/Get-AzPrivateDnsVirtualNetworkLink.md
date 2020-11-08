---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242914"
---
# <span data-ttu-id="148b6-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="148b6-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="148b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="148b6-102">SYNOPSIS</span></span>
<span data-ttu-id="148b6-103">Возвращает ссылку на виртуальную сеть, связанную с указанной частной зоной DNS.</span><span class="sxs-lookup"><span data-stu-id="148b6-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="148b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="148b6-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="148b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="148b6-105">DESCRIPTION</span></span>
<span data-ttu-id="148b6-106">Командлет **Get-AzPrivateDnsVirtualNetworkLink** получает ссылки на виртуальные сетевые сети, связанные с определенной частной зоной DNS из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="148b6-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="148b6-107">Если указан параметр *Name* , возвращается один объект **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="148b6-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="148b6-108">Если параметр *Name* не указан, возвращается массив, содержащий все ссылки, связанные с зоной в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="148b6-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="148b6-109">Вы можете использовать объект **PSPrivateDnsVirtualNetworkLink** для обновления ссылки.</span><span class="sxs-lookup"><span data-stu-id="148b6-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="148b6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="148b6-110">EXAMPLES</span></span>

### <span data-ttu-id="148b6-111">Пример 1: получение ссылки на виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="148b6-111">Example 1: Get a virtual network link.</span></span>
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

<span data-ttu-id="148b6-112">В этом примере показано, как вы получаете mylinkную ссылку на виртуальную сеть, связанную с частной зоной DNS с именем myzone.com из указанной группы ресурсов, и затем сохраняет ее в переменной $Link.</span><span class="sxs-lookup"><span data-stu-id="148b6-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="148b6-113">Пример 2: получение всех ссылок, связанных с зоной, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="148b6-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
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

<span data-ttu-id="148b6-114">Этот пример возвращает все ссылки на виртуальные сетевые сети, связанные с частной DNS-зоной "myzone.com" в указанной группе ресурсов, а затем сохраняет их в переменной $Links.</span><span class="sxs-lookup"><span data-stu-id="148b6-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="148b6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="148b6-115">PARAMETERS</span></span>

### <span data-ttu-id="148b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148b6-116">-DefaultProfile</span></span>
<span data-ttu-id="148b6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="148b6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="148b6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="148b6-118">-Name</span></span>
<span data-ttu-id="148b6-119">Указывает имя ссылки на виртуальную сеть, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="148b6-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="148b6-120">Если вы не укажете значение параметра *Name* , этот командлет получает все ссылки, связанные с указанной частной зоной DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="148b6-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="148b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="148b6-122">Указывает имя группы ресурсов, содержащей ссылку на виртуальную сеть, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="148b6-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="148b6-123">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="148b6-123">-ZoneName</span></span>
<span data-ttu-id="148b6-124">Указывает имя частной зоны DNS, с которой связана виртуальная сетевая связь.</span><span class="sxs-lookup"><span data-stu-id="148b6-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="148b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148b6-125">CommonParameters</span></span>
<span data-ttu-id="148b6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="148b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148b6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="148b6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148b6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="148b6-128">INPUTS</span></span>

### <span data-ttu-id="148b6-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="148b6-129">None</span></span>

## <span data-ttu-id="148b6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="148b6-130">OUTPUTS</span></span>

### <span data-ttu-id="148b6-131">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="148b6-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="148b6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="148b6-132">NOTES</span></span>

## <span data-ttu-id="148b6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="148b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="148b6-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="148b6-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="148b6-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="148b6-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="148b6-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="148b6-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
