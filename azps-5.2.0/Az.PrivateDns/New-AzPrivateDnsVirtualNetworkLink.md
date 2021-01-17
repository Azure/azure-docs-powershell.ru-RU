---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400327"
---
# <span data-ttu-id="3f2da-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3f2da-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="3f2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2da-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2da-103">Создает новую частную виртуальную сеть DNS.</span><span class="sxs-lookup"><span data-stu-id="3f2da-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="3f2da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f2da-104">SYNTAX</span></span>

### <span data-ttu-id="3f2da-105">VirtualNetworkId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f2da-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f2da-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3f2da-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f2da-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3f2da-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2da-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f2da-108">DESCRIPTION</span></span>
<span data-ttu-id="3f2da-109">Командлет **New-AzPrivateDnsVirtualNetworkLink** создает виртуальную сеть DNS в указанной группе ресурсов и закрытой зоне.</span><span class="sxs-lookup"><span data-stu-id="3f2da-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="3f2da-110">Необходимо указать уникальное имя ссылки для параметра *Name,* иначе при этом будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="3f2da-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="3f2da-111">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2da-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3f2da-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f2da-112">EXAMPLES</span></span>

### <span data-ttu-id="3f2da-113">Пример 1. Создание ссылки на частную виртуальную сеть DNS</span><span class="sxs-lookup"><span data-stu-id="3f2da-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="3f2da-114">Эта команда создает виртуальную сетевую связь, связанную с частной зоной DNS myzone.com и виртуальной сетью "myvirtualnetwork" (которая уже была создана в группе ресурсов) в указанной группе ресурсов, а затем сохраняет ее в переменной $Link.</span><span class="sxs-lookup"><span data-stu-id="3f2da-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="3f2da-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f2da-115">PARAMETERS</span></span>

### <span data-ttu-id="3f2da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2da-116">-DefaultProfile</span></span>
<span data-ttu-id="3f2da-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f2da-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f2da-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="3f2da-118">-EnableRegistration</span></span>
<span data-ttu-id="3f2da-119">Параметр переключения, который представляет, включена ли ссылка на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="3f2da-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f2da-120">-Name</span></span>
<span data-ttu-id="3f2da-121">Указывает имя создаемой виртуальной сетевой ссылки.</span><span class="sxs-lookup"><span data-stu-id="3f2da-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="3f2da-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3f2da-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="3f2da-123">ИД ресурса виртуальной сети в другом клиенте.</span><span class="sxs-lookup"><span data-stu-id="3f2da-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2da-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f2da-125">Определяет группу ресурсов, в которой нужно создать связь.</span><span class="sxs-lookup"><span data-stu-id="3f2da-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="3f2da-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f2da-126">-Tag</span></span>
<span data-ttu-id="3f2da-127">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="3f2da-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f2da-128">-VirtualNetwork</span></span>
<span data-ttu-id="3f2da-129">Виртуальный сетевой объект, связанный со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="3f2da-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3f2da-130">-VirtualNetworkId</span></span>
<span data-ttu-id="3f2da-131">ИД ресурса виртуальной сети, связанной со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="3f2da-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3f2da-132">-ZoneName</span></span>
<span data-ttu-id="3f2da-133">Указывает имя зоны, которая будет связана с виртуальной сетевой связью.</span><span class="sxs-lookup"><span data-stu-id="3f2da-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="3f2da-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f2da-134">-Confirm</span></span>
<span data-ttu-id="3f2da-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2da-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2da-136">-WhatIf</span></span>
<span data-ttu-id="3f2da-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2da-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f2da-138">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2da-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f2da-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f2da-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f2da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2da-140">CommonParameters</span></span>
<span data-ttu-id="3f2da-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2da-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f2da-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2da-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f2da-143">INPUTS</span></span>

### <span data-ttu-id="3f2da-144">Нет</span><span class="sxs-lookup"><span data-stu-id="3f2da-144">None</span></span>

## <span data-ttu-id="3f2da-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f2da-145">OUTPUTS</span></span>

### <span data-ttu-id="3f2da-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3f2da-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="3f2da-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f2da-147">NOTES</span></span>

## <span data-ttu-id="3f2da-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f2da-148">RELATED LINKS</span></span>

[<span data-ttu-id="3f2da-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3f2da-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3f2da-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3f2da-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3f2da-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3f2da-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
