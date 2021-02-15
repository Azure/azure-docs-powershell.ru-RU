---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238003"
---
# <span data-ttu-id="ec772-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="ec772-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="ec772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec772-102">SYNOPSIS</span></span>
<span data-ttu-id="ec772-103">Обновив контроллер DevSpaces, добавьте теги.</span><span class="sxs-lookup"><span data-stu-id="ec772-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="ec772-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec772-104">SYNTAX</span></span>

### <span data-ttu-id="ec772-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec772-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec772-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec772-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec772-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec772-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec772-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec772-108">DESCRIPTION</span></span>
<span data-ttu-id="ec772-109">Обновив контроллер DevSpaces, добавьте теги.</span><span class="sxs-lookup"><span data-stu-id="ec772-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="ec772-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec772-110">EXAMPLES</span></span>

### <span data-ttu-id="ec772-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec772-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="ec772-112">Пометка контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="ec772-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="ec772-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec772-113">PARAMETERS</span></span>

### <span data-ttu-id="ec772-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec772-114">-DefaultProfile</span></span>
<span data-ttu-id="ec772-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec772-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec772-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec772-116">-InputObject</span></span>
<span data-ttu-id="ec772-117">Объект PSController, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ec772-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec772-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec772-118">-Name</span></span>
<span data-ttu-id="ec772-119">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="ec772-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="ec772-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec772-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec772-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ec772-121">Resource group name</span></span>

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

### <span data-ttu-id="ec772-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec772-122">-ResourceId</span></span>
<span data-ttu-id="ec772-123">ИД ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="ec772-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="ec772-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec772-124">-Tag</span></span>
<span data-ttu-id="ec772-125">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="ec772-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ec772-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec772-126">-Confirm</span></span>
<span data-ttu-id="ec772-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec772-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec772-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec772-128">-WhatIf</span></span>
<span data-ttu-id="ec772-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec772-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec772-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ec772-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec772-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec772-131">CommonParameters</span></span>
<span data-ttu-id="ec772-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec772-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec772-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec772-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec772-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec772-134">INPUTS</span></span>

### <span data-ttu-id="ec772-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ec772-135">System.String</span></span>

### <span data-ttu-id="ec772-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="ec772-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="ec772-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec772-137">OUTPUTS</span></span>

### <span data-ttu-id="ec772-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="ec772-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="ec772-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec772-139">NOTES</span></span>

## <span data-ttu-id="ec772-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec772-140">RELATED LINKS</span></span>
