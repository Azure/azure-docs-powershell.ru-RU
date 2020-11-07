---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: b6fb42ccafe5b70316ea29251a87b76ea65dda7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721092"
---
# <span data-ttu-id="33d91-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="33d91-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="33d91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33d91-102">SYNOPSIS</span></span>
<span data-ttu-id="33d91-103">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="33d91-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="33d91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33d91-104">SYNTAX</span></span>

### <span data-ttu-id="33d91-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33d91-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d91-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d91-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d91-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d91-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d91-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33d91-108">DESCRIPTION</span></span>
<span data-ttu-id="33d91-109">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="33d91-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="33d91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33d91-110">EXAMPLES</span></span>

### <span data-ttu-id="33d91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33d91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="33d91-112">Удалите контроллер DevSpaces с именем devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="33d91-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="33d91-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33d91-113">PARAMETERS</span></span>

### <span data-ttu-id="33d91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33d91-114">-AsJob</span></span>
<span data-ttu-id="33d91-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33d91-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33d91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d91-116">-DefaultProfile</span></span>
<span data-ttu-id="33d91-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33d91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d91-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d91-118">-InputObject</span></span>
<span data-ttu-id="33d91-119">Объект PSController, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="33d91-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="33d91-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33d91-120">-Name</span></span>
<span data-ttu-id="33d91-121">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="33d91-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="33d91-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d91-122">-PassThru</span></span>
<span data-ttu-id="33d91-123">Возвращает значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="33d91-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="33d91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d91-124">-ResourceGroupName</span></span>
<span data-ttu-id="33d91-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="33d91-125">Resource group name</span></span>

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

### <span data-ttu-id="33d91-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33d91-126">-ResourceId</span></span>
<span data-ttu-id="33d91-127">Идентификатор ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="33d91-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="33d91-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33d91-128">-Confirm</span></span>
<span data-ttu-id="33d91-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="33d91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d91-130">-WhatIf</span></span>
<span data-ttu-id="33d91-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="33d91-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d91-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="33d91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d91-133">CommonParameters</span></span>
<span data-ttu-id="33d91-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33d91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d91-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d91-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d91-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33d91-136">INPUTS</span></span>

### <span data-ttu-id="33d91-137">System. String</span><span class="sxs-lookup"><span data-stu-id="33d91-137">System.String</span></span>

### <span data-ttu-id="33d91-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="33d91-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="33d91-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33d91-139">OUTPUTS</span></span>

### <span data-ttu-id="33d91-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33d91-140">System.Boolean</span></span>

## <span data-ttu-id="33d91-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="33d91-141">NOTES</span></span>

## <span data-ttu-id="33d91-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33d91-142">RELATED LINKS</span></span>
