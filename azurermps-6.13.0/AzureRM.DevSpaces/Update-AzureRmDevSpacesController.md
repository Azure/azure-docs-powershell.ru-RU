---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734132"
---
# <span data-ttu-id="14486-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="14486-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="14486-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14486-102">SYNOPSIS</span></span>
<span data-ttu-id="14486-103">Обновите контроллер DevSpaces, чтобы добавить теги.</span><span class="sxs-lookup"><span data-stu-id="14486-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14486-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14486-104">SYNTAX</span></span>

### <span data-ttu-id="14486-105">DevSpacesControllerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14486-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14486-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14486-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14486-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14486-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14486-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14486-108">DESCRIPTION</span></span>
<span data-ttu-id="14486-109">Обновите контроллер DevSpaces, чтобы добавить теги.</span><span class="sxs-lookup"><span data-stu-id="14486-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="14486-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14486-110">EXAMPLES</span></span>

### <span data-ttu-id="14486-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14486-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="14486-112">Пометьте DevSpacesный звонок.</span><span class="sxs-lookup"><span data-stu-id="14486-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="14486-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14486-113">PARAMETERS</span></span>

### <span data-ttu-id="14486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14486-114">-DefaultProfile</span></span>
<span data-ttu-id="14486-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14486-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14486-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14486-116">-InputObject</span></span>
<span data-ttu-id="14486-117">Объект PSController, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="14486-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="14486-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14486-118">-Name</span></span>
<span data-ttu-id="14486-119">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="14486-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="14486-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14486-120">-ResourceGroupName</span></span>
<span data-ttu-id="14486-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="14486-121">Resource group name</span></span>

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

### <span data-ttu-id="14486-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14486-122">-ResourceId</span></span>
<span data-ttu-id="14486-123">Идентификатор ресурса DevSpaces</span><span class="sxs-lookup"><span data-stu-id="14486-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="14486-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="14486-124">-Tag</span></span>
<span data-ttu-id="14486-125">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14486-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="14486-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14486-126">-Confirm</span></span>
<span data-ttu-id="14486-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14486-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14486-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14486-128">-WhatIf</span></span>
<span data-ttu-id="14486-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14486-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14486-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14486-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14486-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14486-131">CommonParameters</span></span>
<span data-ttu-id="14486-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14486-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14486-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14486-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14486-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14486-134">INPUTS</span></span>

### <span data-ttu-id="14486-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14486-135">System.String</span></span>

### <span data-ttu-id="14486-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="14486-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="14486-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14486-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="14486-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14486-138">OUTPUTS</span></span>

### <span data-ttu-id="14486-139">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="14486-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="14486-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="14486-140">NOTES</span></span>

## <span data-ttu-id="14486-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14486-141">RELATED LINKS</span></span>
