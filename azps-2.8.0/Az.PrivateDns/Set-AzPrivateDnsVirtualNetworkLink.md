---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905045"
---
# <span data-ttu-id="ecac2-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ecac2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecac2-102">SYNOPSIS</span></span>
<span data-ttu-id="ecac2-103">Обновляет или задает ссылку на виртуальную сеть, связанную с частной зоной и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecac2-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="ecac2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecac2-104">SYNTAX</span></span>

### <span data-ttu-id="ecac2-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecac2-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecac2-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="ecac2-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecac2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecac2-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecac2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecac2-108">DESCRIPTION</span></span>
<span data-ttu-id="ecac2-109">Командлет **Set-AzPrivateDnsVirtualNetworkLink** обновляет ссылку, связанную с зоной, из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecac2-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="ecac2-110">Вы можете передать объект **PSPrivateDnsVirtualNetworkLink** с помощью параметра *Link* или оператора Pipeline либо указать *имя* *имя_зоны* и *ResourceGroupName* для параметров.</span><span class="sxs-lookup"><span data-stu-id="ecac2-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ecac2-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ecac2-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ecac2-112">При указании зоны с помощью объекта **PSPrivateDnsVirtualNetworkLink** (который передается через конвейер или параметр *Link* ) ссылка не обновляется, если она была изменена в Azure DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="ecac2-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="ecac2-113">Это обеспечивает защиту для параллельных изменений ссылок.</span><span class="sxs-lookup"><span data-stu-id="ecac2-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="ecac2-114">Это может быть подавлено с помощью параметра *overwrite* , который обновляет ссылку независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="ecac2-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="ecac2-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecac2-115">EXAMPLES</span></span>

### <span data-ttu-id="ecac2-116">Пример 1: Настройка ссылки</span><span class="sxs-lookup"><span data-stu-id="ecac2-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

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

<span data-ttu-id="ecac2-117">Эта команда устанавливает для IsRegistrationEnabled ссылки с именем Mylink, связанной с зоной с именем myzone.com, из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ecac2-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ecac2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecac2-118">PARAMETERS</span></span>

### <span data-ttu-id="ecac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecac2-119">-DefaultProfile</span></span>
<span data-ttu-id="ecac2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ecac2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecac2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecac2-121">-InputObject</span></span>
<span data-ttu-id="ecac2-122">Объект связи виртуальной сети, который нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="ecac2-122">The virtual network link object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="ecac2-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="ecac2-124">Логическое значение, определяющее, включена ли регистрация для ссылки на виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ecac2-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecac2-125">-Name</span></span>
<span data-ttu-id="ecac2-126">Указывает имя ссылки, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="ecac2-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="ecac2-127">Кроме того, необходимо указать параметр *ResourceGroupName* и *zonename* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="ecac2-128">Кроме того, вы можете указать частную DNS-ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ecac2-129">-Overwrite</span></span>
<span data-ttu-id="ecac2-130">При указании ссылки с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается через конвейер или параметр *Link* , ссылка не удаляется, если она была изменена в Azure DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="ecac2-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="ecac2-131">Это обеспечивает защиту для параллельных изменений ссылок.</span><span class="sxs-lookup"><span data-stu-id="ecac2-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="ecac2-132">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению ссылки независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="ecac2-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecac2-133">-ResourceGroupName</span></span>
<span data-ttu-id="ecac2-134">Указывает имя группы ресурсов, которая содержит ссылку для удаления.</span><span class="sxs-lookup"><span data-stu-id="ecac2-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="ecac2-135">Кроме того, необходимо указать параметр *zonename* и *Name* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="ecac2-136">Кроме того, вы можете указать ссылку на виртуальную сеть с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается с помощью конвейера или параметра *ссылки* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecac2-137">-ResourceId</span></span>
<span data-ttu-id="ecac2-138">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="ecac2-138">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="ecac2-139">-Tag</span></span>
<span data-ttu-id="ecac2-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecac2-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ecac2-141">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="ecac2-141">-ZoneName</span></span>
<span data-ttu-id="ecac2-142">Указывает имя DNS-зоны, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ecac2-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="ecac2-143">Кроме того, необходимо указать параметр *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ecac2-144">Кроме того, вы можете указать частную DNS-ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="ecac2-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac2-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecac2-145">-Confirm</span></span>
<span data-ttu-id="ecac2-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecac2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecac2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecac2-147">-WhatIf</span></span>
<span data-ttu-id="ecac2-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecac2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecac2-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecac2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecac2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecac2-150">CommonParameters</span></span>
<span data-ttu-id="ecac2-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecac2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecac2-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecac2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecac2-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecac2-153">INPUTS</span></span>

### <span data-ttu-id="ecac2-154">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="ecac2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ecac2-155">System.String</span></span>

## <span data-ttu-id="ecac2-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecac2-156">OUTPUTS</span></span>

### <span data-ttu-id="ecac2-157">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ecac2-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecac2-158">NOTES</span></span>

## <span data-ttu-id="ecac2-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecac2-159">RELATED LINKS</span></span>

[<span data-ttu-id="ecac2-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ecac2-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ecac2-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecac2-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
