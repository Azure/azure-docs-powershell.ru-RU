---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: e8a9c1f65c536abb3c7b3e7aa983292ccde925a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996316"
---
# <span data-ttu-id="1af54-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1af54-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="1af54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af54-102">SYNOPSIS</span></span>
<span data-ttu-id="1af54-103">Удаляет Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="1af54-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="1af54-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1af54-104">SYNTAX</span></span>

### <span data-ttu-id="1af54-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af54-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af54-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af54-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af54-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af54-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af54-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af54-108">DESCRIPTION</span></span>
<span data-ttu-id="1af54-109">**Cmdlet Remove-AzIpAllocation** удаляет службу IpAllocation Azure.</span><span class="sxs-lookup"><span data-stu-id="1af54-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="1af54-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1af54-110">EXAMPLES</span></span>

### <span data-ttu-id="1af54-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1af54-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="1af54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af54-112">PARAMETERS</span></span>

### <span data-ttu-id="1af54-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af54-113">-AsJob</span></span>
<span data-ttu-id="1af54-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1af54-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1af54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af54-115">-DefaultProfile</span></span>
<span data-ttu-id="1af54-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af54-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1af54-117">-Force</span></span>
<span data-ttu-id="1af54-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1af54-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1af54-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af54-119">-InputObject</span></span>
<span data-ttu-id="1af54-120">{{ Заполнить описание inputObject }}</span><span class="sxs-lookup"><span data-stu-id="1af54-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="1af54-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1af54-121">-Name</span></span>
<span data-ttu-id="1af54-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="1af54-122">The resource name.</span></span>

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

### <span data-ttu-id="1af54-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1af54-123">-PassThru</span></span>
<span data-ttu-id="1af54-124">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1af54-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1af54-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1af54-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1af54-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af54-126">-ResourceGroupName</span></span>
<span data-ttu-id="1af54-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1af54-127">The resource group name.</span></span>

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

### <span data-ttu-id="1af54-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af54-128">-ResourceId</span></span>
<span data-ttu-id="1af54-129">ID ресурса IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="1af54-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="1af54-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af54-130">-Confirm</span></span>
<span data-ttu-id="1af54-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af54-132">-WhatIf</span></span>
<span data-ttu-id="1af54-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af54-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af54-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1af54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af54-135">CommonParameters</span></span>
<span data-ttu-id="1af54-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af54-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1af54-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af54-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1af54-138">INPUTS</span></span>

### <span data-ttu-id="1af54-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1af54-139">System.String</span></span>

## <span data-ttu-id="1af54-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1af54-140">OUTPUTS</span></span>

### <span data-ttu-id="1af54-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1af54-141">System.Boolean</span></span>

## <span data-ttu-id="1af54-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1af54-142">NOTES</span></span>

## <span data-ttu-id="1af54-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af54-143">RELATED LINKS</span></span>
