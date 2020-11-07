---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730128"
---
# <span data-ttu-id="bb57b-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="bb57b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb57b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb57b-103">Удаление префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="bb57b-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="bb57b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb57b-104">SYNTAX</span></span>

### <span data-ttu-id="bb57b-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb57b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb57b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb57b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb57b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb57b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb57b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb57b-108">DESCRIPTION</span></span>
<span data-ttu-id="bb57b-109">Командлет **Remove-AzPublicIpPrefix** удаляет префикс общедоступного IP-адреса Azure, так как в нем нет общедоступных IP-адресов, выделены от него.</span><span class="sxs-lookup"><span data-stu-id="bb57b-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="bb57b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb57b-110">EXAMPLES</span></span>

### <span data-ttu-id="bb57b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb57b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="bb57b-112">Удаление префикса общедоступного IP-адреса с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="bb57b-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="bb57b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb57b-113">PARAMETERS</span></span>

### <span data-ttu-id="bb57b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb57b-114">-AsJob</span></span>
<span data-ttu-id="bb57b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bb57b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb57b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb57b-116">-DefaultProfile</span></span>
<span data-ttu-id="bb57b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb57b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb57b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bb57b-118">-Force</span></span>
<span data-ttu-id="bb57b-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bb57b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bb57b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb57b-120">-InputObject</span></span>
<span data-ttu-id="bb57b-121">Объект PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb57b-122">-Name</span></span>
<span data-ttu-id="bb57b-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb57b-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb57b-124">-PassThru</span></span>
<span data-ttu-id="bb57b-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="bb57b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb57b-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bb57b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb57b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb57b-127">-ResourceGroupName</span></span>
<span data-ttu-id="bb57b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb57b-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb57b-129">-ResourceId</span></span>
<span data-ttu-id="bb57b-130">ResourceId для ресурса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bb57b-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb57b-131">-Confirm</span></span>
<span data-ttu-id="bb57b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb57b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb57b-133">-WhatIf</span></span>
<span data-ttu-id="bb57b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb57b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb57b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb57b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb57b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb57b-136">CommonParameters</span></span>
<span data-ttu-id="bb57b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb57b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb57b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb57b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb57b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb57b-139">INPUTS</span></span>

### <span data-ttu-id="bb57b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bb57b-140">System.String</span></span>

### <span data-ttu-id="bb57b-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="bb57b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb57b-142">OUTPUTS</span></span>

### <span data-ttu-id="bb57b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb57b-143">System.Boolean</span></span>

## <span data-ttu-id="bb57b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb57b-144">NOTES</span></span>

## <span data-ttu-id="bb57b-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb57b-145">RELATED LINKS</span></span>

[<span data-ttu-id="bb57b-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="bb57b-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="bb57b-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="bb57b-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
