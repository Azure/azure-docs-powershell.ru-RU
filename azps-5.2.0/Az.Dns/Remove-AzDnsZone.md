---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402327"
---
# <span data-ttu-id="a07f8-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a07f8-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="a07f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a07f8-103">Удаляет зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a07f8-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="a07f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a07f8-104">SYNTAX</span></span>

### <span data-ttu-id="a07f8-105">Поля</span><span class="sxs-lookup"><span data-stu-id="a07f8-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a07f8-106">Объект</span><span class="sxs-lookup"><span data-stu-id="a07f8-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07f8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a07f8-107">DESCRIPTION</span></span>
<span data-ttu-id="a07f8-108">**Cmdlet Remove-AzDnsZone** окончательно удаляет зону службы доменных имен (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a07f8-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="a07f8-109">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="a07f8-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="a07f8-110">Передать объект **DnsZone** можно с помощью параметра *Name* или с помощью оператора конвейера. Кроме того, можно указать параметры *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="a07f8-111">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07f8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a07f8-112">При указании зоны с использованием объекта **DnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта  **DnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются).</span><span class="sxs-lookup"><span data-stu-id="a07f8-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a07f8-113">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="a07f8-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a07f8-114">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="a07f8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="a07f8-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a07f8-115">EXAMPLES</span></span>

### <span data-ttu-id="a07f8-116">Пример 1. Удаление зоны</span><span class="sxs-lookup"><span data-stu-id="a07f8-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a07f8-117">Эта команда удаляет зону с именем myzone.com из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a07f8-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a07f8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07f8-118">PARAMETERS</span></span>

### <span data-ttu-id="a07f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07f8-119">-DefaultProfile</span></span>
<span data-ttu-id="a07f8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a07f8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a07f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a07f8-121">-Name</span></span>
<span data-ttu-id="a07f8-122">Указывает имя зоны DNS, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07f8-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="a07f8-123">Необходимо также указать параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a07f8-124">Кроме того, вы можете указать зону DNS с помощью *параметра Zone.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07f8-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a07f8-125">-Overwrite</span></span>
<span data-ttu-id="a07f8-126">При указании зоны с использованием объекта **DnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта  **DnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются).</span><span class="sxs-lookup"><span data-stu-id="a07f8-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a07f8-127">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="a07f8-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a07f8-128">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="a07f8-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="a07f8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a07f8-129">-PassThru</span></span>
<span data-ttu-id="a07f8-130">passthru</span><span class="sxs-lookup"><span data-stu-id="a07f8-130">passthru</span></span>

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

### <span data-ttu-id="a07f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="a07f8-132">Имя группы ресурсов, которая содержит удаляемую зону.</span><span class="sxs-lookup"><span data-stu-id="a07f8-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="a07f8-133">Необходимо также указать *параметр ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="a07f8-134">Кроме того, вы можете указать зону DNS с помощью объекта **DnsZone,** переданного через канал или *параметр Zone.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07f8-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="a07f8-135">-Zone</span></span>
<span data-ttu-id="a07f8-136">Определяет зону DNS, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a07f8-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="a07f8-137">Переданный **объект DnsZone** также можно передать через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a07f8-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="a07f8-138">Вы также можете указать зону DNS, которая будет удалена, с помощью параметров *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="a07f8-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a07f8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a07f8-139">-Confirm</span></span>
<span data-ttu-id="a07f8-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07f8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07f8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07f8-141">-WhatIf</span></span>
<span data-ttu-id="a07f8-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07f8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07f8-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a07f8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07f8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07f8-144">CommonParameters</span></span>
<span data-ttu-id="a07f8-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07f8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07f8-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07f8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07f8-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a07f8-147">INPUTS</span></span>

### <span data-ttu-id="a07f8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a07f8-148">System.String</span></span>

### <span data-ttu-id="a07f8-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="a07f8-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="a07f8-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a07f8-150">OUTPUTS</span></span>

### <span data-ttu-id="a07f8-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a07f8-151">System.Boolean</span></span>

## <span data-ttu-id="a07f8-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a07f8-152">NOTES</span></span>
<span data-ttu-id="a07f8-153">В связи с потенциально высоким влиянием удаления зоны DNS по умолчанию этот $ConfirmPreference Windows PowerShell запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a07f8-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="a07f8-154">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="a07f8-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a07f8-155">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="a07f8-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="a07f8-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a07f8-156">RELATED LINKS</span></span>

[<span data-ttu-id="a07f8-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a07f8-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="a07f8-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a07f8-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="a07f8-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a07f8-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
