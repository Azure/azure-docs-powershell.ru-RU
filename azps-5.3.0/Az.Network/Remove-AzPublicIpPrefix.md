---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519958"
---
# <span data-ttu-id="f1943-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f1943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1943-102">SYNOPSIS</span></span>
<span data-ttu-id="f1943-103">Удаление префикса общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="f1943-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="f1943-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1943-104">SYNTAX</span></span>

### <span data-ttu-id="f1943-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1943-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1943-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1943-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1943-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1943-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1943-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1943-108">DESCRIPTION</span></span>
<span data-ttu-id="f1943-109">При этом общедоступный **IP-префикс** Azure удаляется, если из него не выделены общедоступные IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f1943-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="f1943-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1943-110">EXAMPLES</span></span>

### <span data-ttu-id="f1943-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1943-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="f1943-112">Удаляет общедоступный IP-префикс с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="f1943-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="f1943-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1943-113">PARAMETERS</span></span>

### <span data-ttu-id="f1943-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1943-114">-AsJob</span></span>
<span data-ttu-id="f1943-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f1943-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1943-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1943-116">-DefaultProfile</span></span>
<span data-ttu-id="f1943-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1943-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1943-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1943-118">-Force</span></span>
<span data-ttu-id="f1943-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f1943-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1943-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1943-120">-InputObject</span></span>
<span data-ttu-id="f1943-121">Объект PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-121">A PublicIpPrefix object</span></span>

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

### <span data-ttu-id="f1943-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f1943-122">-Name</span></span>
<span data-ttu-id="f1943-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f1943-123">The resource name.</span></span>

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

### <span data-ttu-id="f1943-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1943-124">-PassThru</span></span>
<span data-ttu-id="f1943-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f1943-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1943-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f1943-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1943-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1943-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1943-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1943-128">The resource group name.</span></span>

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

### <span data-ttu-id="f1943-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1943-129">-ResourceId</span></span>
<span data-ttu-id="f1943-130">ИД ресурса, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="f1943-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="f1943-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1943-131">-Confirm</span></span>
<span data-ttu-id="f1943-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1943-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1943-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1943-133">-WhatIf</span></span>
<span data-ttu-id="f1943-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1943-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1943-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1943-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1943-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1943-136">CommonParameters</span></span>
<span data-ttu-id="f1943-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1943-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1943-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1943-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1943-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1943-139">INPUTS</span></span>

### <span data-ttu-id="f1943-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f1943-140">System.String</span></span>

### <span data-ttu-id="f1943-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f1943-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1943-142">OUTPUTS</span></span>

### <span data-ttu-id="f1943-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1943-143">System.Boolean</span></span>

## <span data-ttu-id="f1943-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1943-144">NOTES</span></span>

## <span data-ttu-id="f1943-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1943-145">RELATED LINKS</span></span>

[<span data-ttu-id="f1943-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="f1943-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="f1943-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f1943-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
