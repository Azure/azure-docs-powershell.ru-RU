---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734135"
---
# <span data-ttu-id="6b635-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6b635-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="6b635-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b635-102">SYNOPSIS</span></span>
<span data-ttu-id="6b635-103">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6b635-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b635-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b635-104">SYNTAX</span></span>

### <span data-ttu-id="6b635-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b635-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b635-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b635-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b635-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b635-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b635-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b635-108">DESCRIPTION</span></span>
<span data-ttu-id="6b635-109">Удалите контроллер DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6b635-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="6b635-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b635-110">EXAMPLES</span></span>

### <span data-ttu-id="6b635-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b635-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="6b635-112">Удалите контроллер DevSpaces с именем devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="6b635-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="6b635-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b635-113">PARAMETERS</span></span>

### <span data-ttu-id="6b635-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b635-114">-AsJob</span></span>
<span data-ttu-id="6b635-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6b635-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b635-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b635-116">-DefaultProfile</span></span>
<span data-ttu-id="6b635-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b635-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b635-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b635-118">-InputObject</span></span>
<span data-ttu-id="6b635-119">Объект PSController, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6b635-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b635-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b635-120">-Name</span></span>
<span data-ttu-id="6b635-121">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6b635-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="6b635-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b635-122">-PassThru</span></span>
<span data-ttu-id="6b635-123">Возвращает значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="6b635-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="6b635-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b635-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b635-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6b635-125">Resource group name</span></span>

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

### <span data-ttu-id="6b635-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b635-126">-ResourceId</span></span>
<span data-ttu-id="6b635-127">Идентификатор ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="6b635-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="6b635-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b635-128">-Confirm</span></span>
<span data-ttu-id="6b635-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b635-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b635-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b635-130">-WhatIf</span></span>
<span data-ttu-id="6b635-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b635-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b635-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b635-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b635-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b635-133">CommonParameters</span></span>
<span data-ttu-id="6b635-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b635-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b635-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b635-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b635-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b635-136">INPUTS</span></span>

### <span data-ttu-id="6b635-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6b635-137">System.String</span></span>

### <span data-ttu-id="6b635-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="6b635-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="6b635-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b635-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6b635-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b635-140">OUTPUTS</span></span>

### <span data-ttu-id="6b635-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b635-141">System.Boolean</span></span>

## <span data-ttu-id="6b635-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b635-142">NOTES</span></span>

## <span data-ttu-id="6b635-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b635-143">RELATED LINKS</span></span>
