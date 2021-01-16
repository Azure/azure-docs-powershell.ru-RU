---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424879"
---
# <span data-ttu-id="2e94a-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2e94a-101">Remove-AzPeering</span></span>

## <span data-ttu-id="2e94a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e94a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e94a-103">Удаление пиринга.</span><span class="sxs-lookup"><span data-stu-id="2e94a-103">Delete or remove a peering.</span></span> <span data-ttu-id="2e94a-104">При этом будут удалены все детские ресурсы или оповещения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e94a-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="2e94a-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e94a-105">SYNTAX</span></span>

### <span data-ttu-id="2e94a-106">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e94a-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e94a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2e94a-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e94a-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e94a-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e94a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e94a-109">DESCRIPTION</span></span>
<span data-ttu-id="2e94a-110">Удаление ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="2e94a-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="2e94a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e94a-111">EXAMPLES</span></span>

### <span data-ttu-id="2e94a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e94a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="2e94a-113">Удаление пиринга по иду ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e94a-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="2e94a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e94a-114">PARAMETERS</span></span>

### <span data-ttu-id="2e94a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e94a-115">-AsJob</span></span>
<span data-ttu-id="2e94a-116">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="2e94a-116">Run in the background.</span></span>

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

### <span data-ttu-id="2e94a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e94a-117">-DefaultProfile</span></span>
<span data-ttu-id="2e94a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e94a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e94a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2e94a-119">-Force</span></span>
<span data-ttu-id="2e94a-120">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="2e94a-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="2e94a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e94a-121">-InputObject</span></span>
<span data-ttu-id="2e94a-122">Используйте Get-AzPeering для извлечения этого объекта.</span><span class="sxs-lookup"><span data-stu-id="2e94a-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e94a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e94a-123">-Name</span></span>
<span data-ttu-id="2e94a-124">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2e94a-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e94a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e94a-125">-PassThru</span></span>
<span data-ttu-id="2e94a-126">Возврат к истинам, если они завершены</span><span class="sxs-lookup"><span data-stu-id="2e94a-126">Return true if complete</span></span>

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

### <span data-ttu-id="2e94a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e94a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e94a-128">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e94a-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e94a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e94a-129">-ResourceId</span></span>
<span data-ttu-id="2e94a-130">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="2e94a-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e94a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e94a-131">-Confirm</span></span>
<span data-ttu-id="2e94a-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e94a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e94a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e94a-133">-WhatIf</span></span>
<span data-ttu-id="2e94a-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e94a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e94a-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e94a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e94a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e94a-136">CommonParameters</span></span>
<span data-ttu-id="2e94a-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e94a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e94a-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e94a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e94a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e94a-139">INPUTS</span></span>

### <span data-ttu-id="2e94a-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2e94a-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="2e94a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2e94a-141">System.String</span></span>

## <span data-ttu-id="2e94a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e94a-142">OUTPUTS</span></span>

### <span data-ttu-id="2e94a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e94a-143">System.Boolean</span></span>

## <span data-ttu-id="2e94a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e94a-144">NOTES</span></span>

## <span data-ttu-id="2e94a-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e94a-145">RELATED LINKS</span></span>
