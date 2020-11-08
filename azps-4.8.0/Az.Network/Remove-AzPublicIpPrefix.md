---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236009"
---
# <span data-ttu-id="41427-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="41427-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41427-102">SYNOPSIS</span></span>
<span data-ttu-id="41427-103">Удаление префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="41427-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="41427-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41427-104">SYNTAX</span></span>

### <span data-ttu-id="41427-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41427-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41427-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41427-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41427-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41427-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41427-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41427-108">DESCRIPTION</span></span>
<span data-ttu-id="41427-109">Командлет **Remove-AzPublicIpPrefix** удаляет префикс общедоступного IP-адреса Azure, так как в нем нет общедоступных IP-адресов, выделены от него.</span><span class="sxs-lookup"><span data-stu-id="41427-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="41427-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41427-110">EXAMPLES</span></span>

### <span data-ttu-id="41427-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41427-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="41427-112">Удаление префикса общедоступного IP-адреса с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="41427-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="41427-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41427-113">PARAMETERS</span></span>

### <span data-ttu-id="41427-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41427-114">-AsJob</span></span>
<span data-ttu-id="41427-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41427-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41427-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41427-116">-DefaultProfile</span></span>
<span data-ttu-id="41427-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41427-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41427-118">-Force</span><span class="sxs-lookup"><span data-stu-id="41427-118">-Force</span></span>
<span data-ttu-id="41427-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="41427-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="41427-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41427-120">-InputObject</span></span>
<span data-ttu-id="41427-121">Объект PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="41427-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41427-122">-Name</span></span>
<span data-ttu-id="41427-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="41427-123">The resource name.</span></span>

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

### <span data-ttu-id="41427-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41427-124">-PassThru</span></span>
<span data-ttu-id="41427-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="41427-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="41427-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="41427-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41427-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41427-127">-ResourceGroupName</span></span>
<span data-ttu-id="41427-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41427-128">The resource group name.</span></span>

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

### <span data-ttu-id="41427-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41427-129">-ResourceId</span></span>
<span data-ttu-id="41427-130">ResourceId для ресурса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="41427-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="41427-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41427-131">-Confirm</span></span>
<span data-ttu-id="41427-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41427-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41427-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41427-133">-WhatIf</span></span>
<span data-ttu-id="41427-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41427-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41427-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41427-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41427-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41427-136">CommonParameters</span></span>
<span data-ttu-id="41427-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41427-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41427-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41427-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41427-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41427-139">INPUTS</span></span>

### <span data-ttu-id="41427-140">System. String</span><span class="sxs-lookup"><span data-stu-id="41427-140">System.String</span></span>

### <span data-ttu-id="41427-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="41427-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41427-142">OUTPUTS</span></span>

### <span data-ttu-id="41427-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41427-143">System.Boolean</span></span>

## <span data-ttu-id="41427-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="41427-144">NOTES</span></span>

## <span data-ttu-id="41427-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41427-145">RELATED LINKS</span></span>

[<span data-ttu-id="41427-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="41427-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="41427-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41427-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
