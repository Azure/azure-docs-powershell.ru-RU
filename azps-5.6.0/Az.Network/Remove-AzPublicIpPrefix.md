---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: f3072871caa5449606afe18093a463fea58c6dfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976627"
---
# <span data-ttu-id="36fe0-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="36fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="36fe0-103">Удаление префикса общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="36fe0-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="36fe0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36fe0-104">SYNTAX</span></span>

### <span data-ttu-id="36fe0-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36fe0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fe0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fe0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fe0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36fe0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36fe0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36fe0-108">DESCRIPTION</span></span>
<span data-ttu-id="36fe0-109">При этом общедоступный **IP-префикс** Azure удаляется, если из него не выделены общедоступные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="36fe0-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="36fe0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36fe0-110">EXAMPLES</span></span>

### <span data-ttu-id="36fe0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36fe0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="36fe0-112">Удаляет общедоступный IP-префикс с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="36fe0-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="36fe0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36fe0-113">PARAMETERS</span></span>

### <span data-ttu-id="36fe0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36fe0-114">-AsJob</span></span>
<span data-ttu-id="36fe0-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="36fe0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36fe0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fe0-116">-DefaultProfile</span></span>
<span data-ttu-id="36fe0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36fe0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36fe0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36fe0-118">-Force</span></span>
<span data-ttu-id="36fe0-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="36fe0-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36fe0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36fe0-120">-InputObject</span></span>
<span data-ttu-id="36fe0-121">Объект PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="36fe0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="36fe0-122">-Name</span></span>
<span data-ttu-id="36fe0-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="36fe0-123">The resource name.</span></span>

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

### <span data-ttu-id="36fe0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36fe0-124">-PassThru</span></span>
<span data-ttu-id="36fe0-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="36fe0-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36fe0-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36fe0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36fe0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fe0-127">-ResourceGroupName</span></span>
<span data-ttu-id="36fe0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36fe0-128">The resource group name.</span></span>

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

### <span data-ttu-id="36fe0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36fe0-129">-ResourceId</span></span>
<span data-ttu-id="36fe0-130">ИД ресурса, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="36fe0-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="36fe0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36fe0-131">-Confirm</span></span>
<span data-ttu-id="36fe0-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36fe0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fe0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fe0-133">-WhatIf</span></span>
<span data-ttu-id="36fe0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36fe0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36fe0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36fe0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fe0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fe0-136">CommonParameters</span></span>
<span data-ttu-id="36fe0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fe0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fe0-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36fe0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fe0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36fe0-139">INPUTS</span></span>

### <span data-ttu-id="36fe0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="36fe0-140">System.String</span></span>

### <span data-ttu-id="36fe0-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="36fe0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36fe0-142">OUTPUTS</span></span>

### <span data-ttu-id="36fe0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36fe0-143">System.Boolean</span></span>

## <span data-ttu-id="36fe0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36fe0-144">NOTES</span></span>

## <span data-ttu-id="36fe0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36fe0-145">RELATED LINKS</span></span>

[<span data-ttu-id="36fe0-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="36fe0-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="36fe0-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="36fe0-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
