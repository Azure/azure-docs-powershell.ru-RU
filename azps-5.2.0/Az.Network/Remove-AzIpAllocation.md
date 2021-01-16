---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412759"
---
# <span data-ttu-id="86651-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="86651-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="86651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86651-102">SYNOPSIS</span></span>
<span data-ttu-id="86651-103">Удаляет Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="86651-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="86651-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86651-104">SYNTAX</span></span>

### <span data-ttu-id="86651-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86651-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86651-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86651-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86651-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86651-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86651-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86651-108">DESCRIPTION</span></span>
<span data-ttu-id="86651-109">**Cmdlet Remove-AzIpAllocation** удаляет службу IpAllocation Azure.</span><span class="sxs-lookup"><span data-stu-id="86651-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="86651-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86651-110">EXAMPLES</span></span>

### <span data-ttu-id="86651-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86651-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="86651-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86651-112">PARAMETERS</span></span>

### <span data-ttu-id="86651-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86651-113">-AsJob</span></span>
<span data-ttu-id="86651-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="86651-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86651-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86651-115">-DefaultProfile</span></span>
<span data-ttu-id="86651-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86651-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86651-117">-Force</span><span class="sxs-lookup"><span data-stu-id="86651-117">-Force</span></span>
<span data-ttu-id="86651-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="86651-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86651-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86651-119">-InputObject</span></span>
<span data-ttu-id="86651-120">{{ Заполнить описание inputObject }}</span><span class="sxs-lookup"><span data-stu-id="86651-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86651-121">-Name</span><span class="sxs-lookup"><span data-stu-id="86651-121">-Name</span></span>
<span data-ttu-id="86651-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="86651-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86651-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86651-123">-PassThru</span></span>
<span data-ttu-id="86651-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="86651-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86651-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86651-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86651-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86651-126">-ResourceGroupName</span></span>
<span data-ttu-id="86651-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86651-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86651-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86651-128">-ResourceId</span></span>
<span data-ttu-id="86651-129">ID ресурса IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="86651-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="86651-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86651-130">-Confirm</span></span>
<span data-ttu-id="86651-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="86651-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86651-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86651-132">-WhatIf</span></span>
<span data-ttu-id="86651-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86651-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86651-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86651-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86651-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86651-135">CommonParameters</span></span>
<span data-ttu-id="86651-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86651-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86651-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86651-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86651-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86651-138">INPUTS</span></span>

### <span data-ttu-id="86651-139">System.String</span><span class="sxs-lookup"><span data-stu-id="86651-139">System.String</span></span>

## <span data-ttu-id="86651-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86651-140">OUTPUTS</span></span>

### <span data-ttu-id="86651-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86651-141">System.Boolean</span></span>

## <span data-ttu-id="86651-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86651-142">NOTES</span></span>

## <span data-ttu-id="86651-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86651-143">RELATED LINKS</span></span>
