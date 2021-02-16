---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: eb5c139aea0520df77bf86af01bc3c02f8118263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239997"
---
# <span data-ttu-id="8bd2f-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8bd2f-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="8bd2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd2f-103">Удалите службу поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8bd2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bd2f-104">SYNTAX</span></span>

### <span data-ttu-id="8bd2f-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bd2f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bd2f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bd2f-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bd2f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bd2f-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd2f-108">DESCRIPTION</span></span>
<span data-ttu-id="8bd2f-109">С **помощью cmdlet Remove-AzSearchService** удаляется служба azure Cognitive Search с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="8bd2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bd2f-110">EXAMPLES</span></span>

### <span data-ttu-id="8bd2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bd2f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="8bd2f-112">В этом примере удаляется служба поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8bd2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bd2f-113">PARAMETERS</span></span>

### <span data-ttu-id="8bd2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd2f-114">-DefaultProfile</span></span>
<span data-ttu-id="8bd2f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd2f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8bd2f-116">-Force</span></span>
<span data-ttu-id="8bd2f-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8bd2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bd2f-118">-InputObject</span></span>
<span data-ttu-id="8bd2f-119">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd2f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8bd2f-120">-Name</span></span>
<span data-ttu-id="8bd2f-121">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-121">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd2f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bd2f-122">-PassThru</span></span>
<span data-ttu-id="8bd2f-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8bd2f-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8bd2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd2f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8bd2f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd2f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bd2f-127">-ResourceId</span></span>
<span data-ttu-id="8bd2f-128">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd2f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bd2f-129">-Confirm</span></span>
<span data-ttu-id="8bd2f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd2f-131">-WhatIf</span></span>
<span data-ttu-id="8bd2f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd2f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd2f-134">CommonParameters</span></span>
<span data-ttu-id="8bd2f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd2f-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bd2f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd2f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bd2f-137">INPUTS</span></span>

### <span data-ttu-id="8bd2f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8bd2f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8bd2f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8bd2f-139">System.String</span></span>

## <span data-ttu-id="8bd2f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bd2f-140">OUTPUTS</span></span>

### <span data-ttu-id="8bd2f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd2f-141">System.Boolean</span></span>

## <span data-ttu-id="8bd2f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bd2f-142">NOTES</span></span>

## <span data-ttu-id="8bd2f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bd2f-143">RELATED LINKS</span></span>

[<span data-ttu-id="8bd2f-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8bd2f-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="8bd2f-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8bd2f-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="8bd2f-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8bd2f-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
