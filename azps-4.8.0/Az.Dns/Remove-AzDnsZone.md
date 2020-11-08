---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243605"
---
# <span data-ttu-id="7acc8-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7acc8-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="7acc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7acc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7acc8-103">Удаляет зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7acc8-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="7acc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7acc8-104">SYNTAX</span></span>

### <span data-ttu-id="7acc8-105">»</span><span class="sxs-lookup"><span data-stu-id="7acc8-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acc8-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="7acc8-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7acc8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7acc8-107">DESCRIPTION</span></span>
<span data-ttu-id="7acc8-108">Командлет **Remove-AzDnsZone** окончательно УДАЛЯЕТ зону DNS из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7acc8-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="7acc8-109">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="7acc8-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="7acc8-110">Вы можете передать объект **dnsZone** с помощью параметра *Name* или оператора Pipeline либо указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7acc8-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7acc8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7acc8-112">При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="7acc8-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7acc8-113">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="7acc8-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7acc8-114">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="7acc8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="7acc8-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7acc8-115">EXAMPLES</span></span>

### <span data-ttu-id="7acc8-116">Пример 1: Удаление зоны</span><span class="sxs-lookup"><span data-stu-id="7acc8-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7acc8-117">Эта команда удаляет зону с именем myzone.com из группы ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7acc8-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7acc8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7acc8-118">PARAMETERS</span></span>

### <span data-ttu-id="7acc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acc8-119">-DefaultProfile</span></span>
<span data-ttu-id="7acc8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7acc8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7acc8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7acc8-121">-Name</span></span>
<span data-ttu-id="7acc8-122">Указывает имя DNS-зоны, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7acc8-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="7acc8-123">Кроме того, необходимо указать параметр *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7acc8-124">Кроме того, вы можете указать зону DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7acc8-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7acc8-125">-Overwrite</span></span>
<span data-ttu-id="7acc8-126">При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="7acc8-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7acc8-127">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="7acc8-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7acc8-128">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="7acc8-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="7acc8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7acc8-129">-PassThru</span></span>
<span data-ttu-id="7acc8-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="7acc8-130">passthru</span></span>

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

### <span data-ttu-id="7acc8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7acc8-131">-ResourceGroupName</span></span>
<span data-ttu-id="7acc8-132">Указывает имя группы ресурсов, содержащей зону, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7acc8-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="7acc8-133">Кроме того, необходимо указать параметр *zonename* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="7acc8-134">Кроме того, вы можете указать зону DNS с помощью объекта **dnsZone** , передаваемого через конвейер или параметр *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7acc8-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="7acc8-135">-Zone</span></span>
<span data-ttu-id="7acc8-136">Указывает зону DNS для удаления.</span><span class="sxs-lookup"><span data-stu-id="7acc8-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="7acc8-137">Переданный объект **dnsZone** также можно передать через конвейер.</span><span class="sxs-lookup"><span data-stu-id="7acc8-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="7acc8-138">Кроме того, вы можете указать зону DNS для удаления с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7acc8-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="7acc8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7acc8-139">-Confirm</span></span>
<span data-ttu-id="7acc8-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7acc8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7acc8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acc8-141">-WhatIf</span></span>
<span data-ttu-id="7acc8-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7acc8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7acc8-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7acc8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7acc8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acc8-144">CommonParameters</span></span>
<span data-ttu-id="7acc8-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7acc8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acc8-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7acc8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acc8-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7acc8-147">INPUTS</span></span>

### <span data-ttu-id="7acc8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7acc8-148">System.String</span></span>

### <span data-ttu-id="7acc8-149">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="7acc8-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="7acc8-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7acc8-150">OUTPUTS</span></span>

### <span data-ttu-id="7acc8-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7acc8-151">System.Boolean</span></span>

## <span data-ttu-id="7acc8-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="7acc8-152">NOTES</span></span>
<span data-ttu-id="7acc8-153">Из-за потенциально высокого воздействия на удаление зоны DNS по умолчанию этот командлет запрашивает подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет любое значение, отличное от None.</span><span class="sxs-lookup"><span data-stu-id="7acc8-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="7acc8-154">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="7acc8-154">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="7acc8-155">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7acc8-155">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="7acc8-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7acc8-156">RELATED LINKS</span></span>

[<span data-ttu-id="7acc8-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7acc8-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="7acc8-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7acc8-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="7acc8-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7acc8-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
