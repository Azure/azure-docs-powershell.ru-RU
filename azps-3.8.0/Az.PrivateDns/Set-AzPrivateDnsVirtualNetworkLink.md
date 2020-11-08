---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065473"
---
# <span data-ttu-id="d24b1-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d24b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d24b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d24b1-103">Обновляет или задает ссылку на виртуальную сеть, связанную с частной зоной и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d24b1-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="d24b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d24b1-104">SYNTAX</span></span>

### <span data-ttu-id="d24b1-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d24b1-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24b1-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="d24b1-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24b1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d24b1-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d24b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d24b1-109">Командлет **Set-AzPrivateDnsVirtualNetworkLink** обновляет ссылку, связанную с зоной, из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d24b1-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="d24b1-110">Вы можете передать объект **PSPrivateDnsVirtualNetworkLink** с помощью параметра *Link* или оператора Pipeline либо указать *имя* *имя_зоны* и *ResourceGroupName* для параметров.</span><span class="sxs-lookup"><span data-stu-id="d24b1-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d24b1-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d24b1-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d24b1-112">При указании зоны с помощью объекта **PSPrivateDnsVirtualNetworkLink** (который передается через конвейер или параметр *Link* ) ссылка не обновляется, если она была изменена в Azure DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="d24b1-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="d24b1-113">Это обеспечивает защиту для параллельных изменений ссылок.</span><span class="sxs-lookup"><span data-stu-id="d24b1-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="d24b1-114">Это может быть подавлено с помощью параметра *overwrite* , который обновляет ссылку независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="d24b1-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="d24b1-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d24b1-115">EXAMPLES</span></span>

### <span data-ttu-id="d24b1-116">Пример 1: Настройка ссылки</span><span class="sxs-lookup"><span data-stu-id="d24b1-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="d24b1-117">Эта команда устанавливает для IsRegistrationEnabled ссылки с именем Mylink, связанной с зоной с именем myzone.com, из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d24b1-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d24b1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d24b1-118">PARAMETERS</span></span>

### <span data-ttu-id="d24b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24b1-119">-DefaultProfile</span></span>
<span data-ttu-id="d24b1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d24b1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d24b1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d24b1-121">-InputObject</span></span>
<span data-ttu-id="d24b1-122">Объект связи виртуальной сети, который нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="d24b1-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="d24b1-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="d24b1-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="d24b1-124">Логическое значение, определяющее, включена ли регистрация для ссылки на виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="d24b1-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="d24b1-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d24b1-125">-Name</span></span>
<span data-ttu-id="d24b1-126">Указывает имя ссылки, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="d24b1-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="d24b1-127">Кроме того, необходимо указать параметр *ResourceGroupName* и *zonename* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="d24b1-128">Кроме того, вы можете указать частную DNS-ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="d24b1-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d24b1-129">-Overwrite</span></span>
<span data-ttu-id="d24b1-130">При указании ссылки с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается через конвейер или параметр *Link* , ссылка не удаляется, если она была изменена в Azure DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="d24b1-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="d24b1-131">Это обеспечивает защиту для параллельных изменений ссылок.</span><span class="sxs-lookup"><span data-stu-id="d24b1-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="d24b1-132">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению ссылки независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="d24b1-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d24b1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24b1-133">-ResourceGroupName</span></span>
<span data-ttu-id="d24b1-134">Указывает имя группы ресурсов, которая содержит ссылку для удаления.</span><span class="sxs-lookup"><span data-stu-id="d24b1-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="d24b1-135">Кроме того, необходимо указать параметр *zonename* и *Name* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="d24b1-136">Кроме того, вы можете указать ссылку на виртуальную сеть с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается с помощью конвейера или параметра *ссылки* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="d24b1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d24b1-137">-ResourceId</span></span>
<span data-ttu-id="d24b1-138">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="d24b1-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="d24b1-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="d24b1-139">-Tag</span></span>
<span data-ttu-id="d24b1-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d24b1-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d24b1-141">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="d24b1-141">-ZoneName</span></span>
<span data-ttu-id="d24b1-142">Указывает имя DNS-зоны, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d24b1-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="d24b1-143">Кроме того, необходимо указать параметр *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="d24b1-144">Кроме того, вы можете указать частную DNS-ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="d24b1-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="d24b1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d24b1-145">-Confirm</span></span>
<span data-ttu-id="d24b1-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d24b1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24b1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24b1-147">-WhatIf</span></span>
<span data-ttu-id="d24b1-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d24b1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24b1-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d24b1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24b1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24b1-150">CommonParameters</span></span>
<span data-ttu-id="d24b1-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d24b1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24b1-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24b1-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24b1-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d24b1-153">INPUTS</span></span>

### <span data-ttu-id="d24b1-154">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="d24b1-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d24b1-155">System.String</span></span>

## <span data-ttu-id="d24b1-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d24b1-156">OUTPUTS</span></span>

### <span data-ttu-id="d24b1-157">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d24b1-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="d24b1-158">NOTES</span></span>

## <span data-ttu-id="d24b1-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d24b1-159">RELATED LINKS</span></span>

[<span data-ttu-id="d24b1-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d24b1-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d24b1-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24b1-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
