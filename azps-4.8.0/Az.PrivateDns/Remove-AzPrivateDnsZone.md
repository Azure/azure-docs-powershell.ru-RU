---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235483"
---
# <span data-ttu-id="1326b-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1326b-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="1326b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1326b-102">SYNOPSIS</span></span>
<span data-ttu-id="1326b-103">Удаление частной зоны DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1326b-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="1326b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1326b-104">SYNTAX</span></span>

### <span data-ttu-id="1326b-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1326b-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1326b-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="1326b-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1326b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1326b-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1326b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1326b-108">DESCRIPTION</span></span>
<span data-ttu-id="1326b-109">Командлет **Remove-AzPrivateDnsZone** окончательно удаляет из заданной группы ресурсов зону DNS частной системы доменных имен.</span><span class="sxs-lookup"><span data-stu-id="1326b-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="1326b-110">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="1326b-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="1326b-111">Вы можете передать объект **PrivateDnsZone** с помощью параметра *PrivateZone* или с помощью оператора конвейера или можно указать параметры *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1326b-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1326b-112">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1326b-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1326b-113">При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **PrivateDnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="1326b-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1326b-114">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="1326b-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1326b-115">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="1326b-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="1326b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1326b-116">EXAMPLES</span></span>

### <span data-ttu-id="1326b-117">Пример 1: Удаление частной зоны</span><span class="sxs-lookup"><span data-stu-id="1326b-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1326b-118">Эта команда удаляет зону с именем myzone.com из группы ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1326b-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="1326b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1326b-119">PARAMETERS</span></span>

### <span data-ttu-id="1326b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1326b-120">-DefaultProfile</span></span>
<span data-ttu-id="1326b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1326b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1326b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1326b-122">-Name</span></span>
<span data-ttu-id="1326b-123">Указывает имя частной DNS-зоны, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1326b-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="1326b-124">Кроме того, необходимо указать параметр *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1326b-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="1326b-125">Кроме того, вы можете указать зону DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="1326b-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1326b-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1326b-126">-Overwrite</span></span>
<span data-ttu-id="1326b-127">При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **PrivateDnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="1326b-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1326b-128">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="1326b-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1326b-129">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="1326b-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1326b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1326b-130">-PassThru</span></span>
<span data-ttu-id="1326b-131">Используется для передачи результата (логического значения) операции Delete My Private Zone дальше вниз по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1326b-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="1326b-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="1326b-132">-PrivateZone</span></span>
<span data-ttu-id="1326b-133">Объект частной зоны, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1326b-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1326b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1326b-134">-ResourceGroupName</span></span>
<span data-ttu-id="1326b-135">Указывает имя группы ресурсов, содержащей зону, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1326b-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="1326b-136">Кроме того, необходимо указать параметр *zonename* .</span><span class="sxs-lookup"><span data-stu-id="1326b-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="1326b-137">Кроме того, вы можете указать зону DNS с помощью объекта **PrivateDnsZone** , передаваемого через конвейер или параметр *Zone* .</span><span class="sxs-lookup"><span data-stu-id="1326b-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1326b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1326b-138">-ResourceId</span></span>
<span data-ttu-id="1326b-139">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="1326b-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="1326b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1326b-140">-Confirm</span></span>
<span data-ttu-id="1326b-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1326b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1326b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1326b-142">-WhatIf</span></span>
<span data-ttu-id="1326b-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1326b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1326b-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1326b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1326b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1326b-145">CommonParameters</span></span>
<span data-ttu-id="1326b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1326b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1326b-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1326b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1326b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1326b-148">INPUTS</span></span>

### <span data-ttu-id="1326b-149">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1326b-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="1326b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1326b-150">System.String</span></span>

## <span data-ttu-id="1326b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1326b-151">OUTPUTS</span></span>

### <span data-ttu-id="1326b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1326b-152">System.Boolean</span></span>

## <span data-ttu-id="1326b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="1326b-153">NOTES</span></span>

## <span data-ttu-id="1326b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1326b-154">RELATED LINKS</span></span>

[<span data-ttu-id="1326b-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1326b-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="1326b-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1326b-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="1326b-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1326b-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)