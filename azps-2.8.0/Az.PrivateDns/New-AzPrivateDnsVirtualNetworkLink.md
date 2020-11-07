---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: a9d14f9d141a1a72accbb43bb35748d1947c3b19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905074"
---
# <span data-ttu-id="b544d-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b544d-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="b544d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b544d-102">SYNOPSIS</span></span>
<span data-ttu-id="b544d-103">Создание ссылки на виртуальную сеть частной DNS.</span><span class="sxs-lookup"><span data-stu-id="b544d-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="b544d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b544d-104">SYNTAX</span></span>

### <span data-ttu-id="b544d-105">VirtualNetworkId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b544d-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b544d-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="b544d-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b544d-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b544d-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b544d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b544d-108">DESCRIPTION</span></span>
<span data-ttu-id="b544d-109">Командлет **New-AzPrivateDnsVirtualNetworkLink** создает новую ссылку на виртуальную сеть доменных имен (DNS) в заданной группе ресурсов и частной зоне.</span><span class="sxs-lookup"><span data-stu-id="b544d-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="b544d-110">Необходимо указать уникальное имя ссылки для параметра *Name* , иначе командлет возвратит ошибку.</span><span class="sxs-lookup"><span data-stu-id="b544d-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="b544d-111">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b544d-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b544d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b544d-112">EXAMPLES</span></span>

### <span data-ttu-id="b544d-113">Пример 1: создание частной ссылки на виртуальную сеть DNS</span><span class="sxs-lookup"><span data-stu-id="b544d-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="b544d-114">Эта команда создает новую ссылку на виртуальную сеть, связанную с частной DNS-зоной с именем myzone.com и виртуальной сетью "myvirtualnetwork" (уже созданной в группе ресурсов) в указанной группе ресурсов, а затем сохраняет ее в переменной $Link.</span><span class="sxs-lookup"><span data-stu-id="b544d-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="b544d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b544d-115">PARAMETERS</span></span>

### <span data-ttu-id="b544d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b544d-116">-DefaultProfile</span></span>
<span data-ttu-id="b544d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b544d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b544d-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="b544d-118">-EnableRegistration</span></span>
<span data-ttu-id="b544d-119">Параметр Switch, обозначающий, включена ли ссылка регистрация.</span><span class="sxs-lookup"><span data-stu-id="b544d-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="b544d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b544d-120">-Name</span></span>
<span data-ttu-id="b544d-121">Указывает имя создаваемой ссылки на виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b544d-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="b544d-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b544d-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="b544d-123">Идентификатор ресурса виртуальной сети в другом клиенте.</span><span class="sxs-lookup"><span data-stu-id="b544d-123">The resource id of the virtual network in another tenant.</span></span>

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

### <span data-ttu-id="b544d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b544d-124">-ResourceGroupName</span></span>
<span data-ttu-id="b544d-125">Указывает группу ресурсов, в которой нужно создать ссылку.</span><span class="sxs-lookup"><span data-stu-id="b544d-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="b544d-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="b544d-126">-Tag</span></span>
<span data-ttu-id="b544d-127">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b544d-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b544d-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b544d-128">-VirtualNetwork</span></span>
<span data-ttu-id="b544d-129">Объект виртуальной сети, связанный со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="b544d-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="b544d-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b544d-130">-VirtualNetworkId</span></span>
<span data-ttu-id="b544d-131">Идентификатор ресурса виртуальной сети, связанной с ссылкой.</span><span class="sxs-lookup"><span data-stu-id="b544d-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="b544d-132">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="b544d-132">-ZoneName</span></span>
<span data-ttu-id="b544d-133">Указывает имя зоны, которая будет связана с ссылкой на виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b544d-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="b544d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b544d-134">-Confirm</span></span>
<span data-ttu-id="b544d-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b544d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b544d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b544d-136">-WhatIf</span></span>
<span data-ttu-id="b544d-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b544d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b544d-138">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b544d-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b544d-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b544d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b544d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b544d-140">CommonParameters</span></span>
<span data-ttu-id="b544d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b544d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b544d-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b544d-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b544d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b544d-143">INPUTS</span></span>

### <span data-ttu-id="b544d-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="b544d-144">None</span></span>

## <span data-ttu-id="b544d-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b544d-145">OUTPUTS</span></span>

### <span data-ttu-id="b544d-146">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b544d-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="b544d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b544d-147">NOTES</span></span>

## <span data-ttu-id="b544d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b544d-148">RELATED LINKS</span></span>

[<span data-ttu-id="b544d-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b544d-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b544d-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b544d-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b544d-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b544d-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
