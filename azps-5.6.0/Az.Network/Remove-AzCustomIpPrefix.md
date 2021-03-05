---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: d4fcdb1ad5606753980ea323137d0b77a8580ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976659"
---
# <span data-ttu-id="35bb2-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="35bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="35bb2-103">Удаление customIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="35bb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35bb2-104">SYNTAX</span></span>

### <span data-ttu-id="35bb2-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35bb2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35bb2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35bb2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35bb2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35bb2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35bb2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35bb2-108">DESCRIPTION</span></span>
<span data-ttu-id="35bb2-109">Для **удаления customIpPrefix удаляется cmdlet Remove-AzCustomIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="35bb2-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="35bb2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="35bb2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35bb2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="35bb2-112">Удаляет customIpPrefix с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="35bb2-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="35bb2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="35bb2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35bb2-114">-AsJob</span></span>
<span data-ttu-id="35bb2-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35bb2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bb2-116">-DefaultProfile</span></span>
<span data-ttu-id="35bb2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35bb2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="35bb2-118">-Force</span></span>
<span data-ttu-id="35bb2-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="35bb2-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35bb2-120">-InputObject</span></span>
<span data-ttu-id="35bb2-121">Настраиваемый объектIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="35bb2-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35bb2-122">-Name</span></span>
<span data-ttu-id="35bb2-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="35bb2-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35bb2-124">-PassThru</span></span>
<span data-ttu-id="35bb2-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="35bb2-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35bb2-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="35bb2-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35bb2-127">-ResourceGroupName</span></span>
<span data-ttu-id="35bb2-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35bb2-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35bb2-129">-ResourceId</span></span>
<span data-ttu-id="35bb2-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="35bb2-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35bb2-131">-Confirm</span></span>
<span data-ttu-id="35bb2-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="35bb2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35bb2-133">-WhatIf</span></span>
<span data-ttu-id="35bb2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35bb2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35bb2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35bb2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bb2-136">CommonParameters</span></span>
<span data-ttu-id="35bb2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35bb2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bb2-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35bb2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bb2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35bb2-139">INPUTS</span></span>

### <span data-ttu-id="35bb2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="35bb2-140">System.String</span></span>

### <span data-ttu-id="35bb2-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="35bb2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35bb2-142">OUTPUTS</span></span>

### <span data-ttu-id="35bb2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35bb2-143">System.Boolean</span></span>

## <span data-ttu-id="35bb2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35bb2-144">NOTES</span></span>

## <span data-ttu-id="35bb2-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35bb2-145">RELATED LINKS</span></span>

[<span data-ttu-id="35bb2-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="35bb2-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="35bb2-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35bb2-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)