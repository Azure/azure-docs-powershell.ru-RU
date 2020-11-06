---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: a9f277c17d0396127ca1b2678d8c9c77ef3628c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568791"
---
# <span data-ttu-id="cffb8-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="cffb8-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="cffb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cffb8-102">SYNOPSIS</span></span>
<span data-ttu-id="cffb8-103">Удаляет зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cffb8-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cffb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cffb8-104">SYNTAX</span></span>

### <span data-ttu-id="cffb8-105">»</span><span class="sxs-lookup"><span data-stu-id="cffb8-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cffb8-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="cffb8-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cffb8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cffb8-107">DESCRIPTION</span></span>
<span data-ttu-id="cffb8-108">Командлет **Remove-AzureRmDnsZone** окончательно УДАЛЯЕТ зону DNS из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cffb8-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="cffb8-109">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="cffb8-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="cffb8-110">Вы можете передать объект **dnsZone** с помощью параметра *Name* или оператора Pipeline либо указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="cffb8-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cffb8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="cffb8-112">При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="cffb8-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="cffb8-113">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="cffb8-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="cffb8-114">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="cffb8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="cffb8-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cffb8-115">EXAMPLES</span></span>

### <span data-ttu-id="cffb8-116">Пример 1: Удаление зоны</span><span class="sxs-lookup"><span data-stu-id="cffb8-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="cffb8-117">Эта команда удаляет зону с именем myzone.com из группы ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cffb8-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="cffb8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cffb8-118">PARAMETERS</span></span>

### <span data-ttu-id="cffb8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cffb8-119">-Force</span></span>
<span data-ttu-id="cffb8-120">Этот параметр устарел для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="cffb8-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="cffb8-121">Оно будет удалено в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cffb8-121">It will be removed in a future release.</span></span>

<span data-ttu-id="cffb8-122">Чтобы указать, будет ли этот командлет запрашивать подтверждение, используйте параметр *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="cffb8-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cffb8-123">-Name</span></span>
<span data-ttu-id="cffb8-124">Указывает имя DNS-зоны, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cffb8-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="cffb8-125">Кроме того, необходимо указать параметр *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="cffb8-126">Кроме того, вы можете указать зону DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="cffb8-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="cffb8-127">-Overwrite</span></span>
<span data-ttu-id="cffb8-128">При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).</span><span class="sxs-lookup"><span data-stu-id="cffb8-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="cffb8-129">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="cffb8-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="cffb8-130">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="cffb8-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="cffb8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cffb8-131">-PassThru</span></span>
<span data-ttu-id="cffb8-132">PassThru</span><span class="sxs-lookup"><span data-stu-id="cffb8-132">passthru</span></span>

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

### <span data-ttu-id="cffb8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffb8-133">-ResourceGroupName</span></span>
<span data-ttu-id="cffb8-134">Указывает имя группы ресурсов, содержащей зону, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cffb8-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="cffb8-135">Кроме того, необходимо указать параметр *zonename* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="cffb8-136">Кроме того, вы можете указать зону DNS с помощью объекта **dnsZone** , передаваемого через конвейер или параметр *Zone* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="cffb8-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="cffb8-137">-Zone</span></span>
<span data-ttu-id="cffb8-138">Указывает зону DNS для удаления.</span><span class="sxs-lookup"><span data-stu-id="cffb8-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="cffb8-139">Переданный объект **dnsZone** также можно передать через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cffb8-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="cffb8-140">Кроме того, вы можете указать зону DNS для удаления с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cffb8-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="cffb8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cffb8-141">-Confirm</span></span>
<span data-ttu-id="cffb8-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cffb8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cffb8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffb8-143">-WhatIf</span></span>
<span data-ttu-id="cffb8-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cffb8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffb8-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cffb8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cffb8-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffb8-146">-DefaultProfile</span></span>
<span data-ttu-id="cffb8-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cffb8-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffb8-148">CommonParameters</span></span>
<span data-ttu-id="cffb8-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cffb8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffb8-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffb8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffb8-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cffb8-151">INPUTS</span></span>

### <span data-ttu-id="cffb8-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="cffb8-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="cffb8-153">Вы можете передать на этот командлет объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="cffb8-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="cffb8-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cffb8-154">OUTPUTS</span></span>

### <span data-ttu-id="cffb8-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="cffb8-155">None</span></span>
<span data-ttu-id="cffb8-156">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cffb8-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cffb8-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="cffb8-157">NOTES</span></span>
<span data-ttu-id="cffb8-158">Из-за потенциально высокого воздействия на удаление зоны DNS по умолчанию этот командлет запрашивает подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет любое значение, отличное от None.</span><span class="sxs-lookup"><span data-stu-id="cffb8-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="cffb8-159">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="cffb8-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="cffb8-160">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cffb8-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="cffb8-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cffb8-161">RELATED LINKS</span></span>

[<span data-ttu-id="cffb8-162">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="cffb8-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="cffb8-163">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="cffb8-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="cffb8-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="cffb8-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
