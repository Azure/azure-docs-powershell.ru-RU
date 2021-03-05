---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: db62779ab2ac03e6ef528b09dda99fb5ebb244a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989302"
---
# <span data-ttu-id="d2df6-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d2df6-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d2df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2df6-102">SYNOPSIS</span></span>
<span data-ttu-id="d2df6-103">Удаление зарегистрированного префикса из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="d2df6-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="d2df6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2df6-104">SYNTAX</span></span>

### <span data-ttu-id="d2df6-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2df6-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2df6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2df6-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2df6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2df6-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2df6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2df6-108">DESCRIPTION</span></span>
<span data-ttu-id="d2df6-109">Позволяет удалить зарегистрированный префикс из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="d2df6-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="d2df6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2df6-110">EXAMPLES</span></span>

### <span data-ttu-id="d2df6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2df6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="d2df6-112">Удаление зарегистрированного префикса по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2df6-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="d2df6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2df6-113">PARAMETERS</span></span>

### <span data-ttu-id="d2df6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2df6-114">-AsJob</span></span>
<span data-ttu-id="d2df6-115">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d2df6-115">Run in the background.</span></span>

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

### <span data-ttu-id="d2df6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2df6-116">-DefaultProfile</span></span>
<span data-ttu-id="d2df6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2df6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2df6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2df6-118">-Force</span></span>
<span data-ttu-id="d2df6-119">Принудительное завершение операции</span><span class="sxs-lookup"><span data-stu-id="d2df6-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="d2df6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2df6-120">-InputObject</span></span>
<span data-ttu-id="d2df6-121">Использование Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d2df6-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2df6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d2df6-122">-Name</span></span>
<span data-ttu-id="d2df6-123">Имя префикса.</span><span class="sxs-lookup"><span data-stu-id="d2df6-123">The name of prefix.</span></span>

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

### <span data-ttu-id="d2df6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2df6-124">-PassThru</span></span>
<span data-ttu-id="d2df6-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d2df6-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d2df6-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d2df6-126">-PeeringName</span></span>
<span data-ttu-id="d2df6-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d2df6-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2df6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2df6-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2df6-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2df6-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d2df6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2df6-130">-ResourceId</span></span>
<span data-ttu-id="d2df6-131">Имя строки "ИД ресурса".</span><span class="sxs-lookup"><span data-stu-id="d2df6-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2df6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2df6-132">-Confirm</span></span>
<span data-ttu-id="d2df6-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d2df6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2df6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2df6-134">-WhatIf</span></span>
<span data-ttu-id="d2df6-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2df6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2df6-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2df6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2df6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2df6-137">CommonParameters</span></span>
<span data-ttu-id="d2df6-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2df6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2df6-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2df6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2df6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2df6-140">INPUTS</span></span>

### <span data-ttu-id="d2df6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d2df6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="d2df6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d2df6-142">System.String</span></span>

## <span data-ttu-id="d2df6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2df6-143">OUTPUTS</span></span>

### <span data-ttu-id="d2df6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2df6-144">System.Boolean</span></span>

## <span data-ttu-id="d2df6-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2df6-145">NOTES</span></span>

## <span data-ttu-id="d2df6-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2df6-146">RELATED LINKS</span></span>
