---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012184"
---
# <span data-ttu-id="58e33-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="58e33-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="58e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e33-102">SYNOPSIS</span></span>
<span data-ttu-id="58e33-103">Обновив контроллер DevSpaces, добавьте теги.</span><span class="sxs-lookup"><span data-stu-id="58e33-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="58e33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58e33-104">SYNTAX</span></span>

### <span data-ttu-id="58e33-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58e33-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e33-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e33-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e33-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e33-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e33-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58e33-108">DESCRIPTION</span></span>
<span data-ttu-id="58e33-109">Обновив контроллер DevSpaces, добавьте теги.</span><span class="sxs-lookup"><span data-stu-id="58e33-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="58e33-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58e33-110">EXAMPLES</span></span>

### <span data-ttu-id="58e33-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58e33-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="58e33-112">Пометка контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="58e33-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="58e33-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e33-113">PARAMETERS</span></span>

### <span data-ttu-id="58e33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e33-114">-DefaultProfile</span></span>
<span data-ttu-id="58e33-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58e33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e33-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e33-116">-InputObject</span></span>
<span data-ttu-id="58e33-117">Объект PSController, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="58e33-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e33-118">-Name</span><span class="sxs-lookup"><span data-stu-id="58e33-118">-Name</span></span>
<span data-ttu-id="58e33-119">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="58e33-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e33-120">-ResourceGroupName</span></span>
<span data-ttu-id="58e33-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="58e33-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e33-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e33-122">-ResourceId</span></span>
<span data-ttu-id="58e33-123">ИД ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="58e33-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e33-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="58e33-124">-Tag</span></span>
<span data-ttu-id="58e33-125">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="58e33-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e33-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e33-126">-Confirm</span></span>
<span data-ttu-id="58e33-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="58e33-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e33-128">-WhatIf</span></span>
<span data-ttu-id="58e33-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58e33-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e33-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="58e33-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e33-131">CommonParameters</span></span>
<span data-ttu-id="58e33-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e33-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e33-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e33-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58e33-134">INPUTS</span></span>

### <span data-ttu-id="58e33-135">System.String</span><span class="sxs-lookup"><span data-stu-id="58e33-135">System.String</span></span>

### <span data-ttu-id="58e33-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="58e33-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="58e33-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58e33-137">OUTPUTS</span></span>

### <span data-ttu-id="58e33-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="58e33-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="58e33-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58e33-139">NOTES</span></span>

## <span data-ttu-id="58e33-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58e33-140">RELATED LINKS</span></span>
