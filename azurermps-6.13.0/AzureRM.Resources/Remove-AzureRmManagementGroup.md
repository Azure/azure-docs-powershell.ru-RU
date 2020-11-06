---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567691"
---
# <span data-ttu-id="bec1b-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="bec1b-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="bec1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bec1b-102">SYNOPSIS</span></span>
<span data-ttu-id="bec1b-103">Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="bec1b-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bec1b-104">SYNTAX</span></span>

### <span data-ttu-id="bec1b-105">GroupOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bec1b-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec1b-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="bec1b-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec1b-107">DESCRIPTION</span></span>
<span data-ttu-id="bec1b-108">Командлет **Remove-AzureRmManagementGroup** удаляет группу управления.</span><span class="sxs-lookup"><span data-stu-id="bec1b-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="bec1b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bec1b-109">EXAMPLES</span></span>

### <span data-ttu-id="bec1b-110">Пример 1: Удаление группы управления</span><span class="sxs-lookup"><span data-stu-id="bec1b-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="bec1b-111">Пример 2: Удаление группы управления с помощью объекта трубопроводов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="bec1b-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="bec1b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bec1b-112">PARAMETERS</span></span>

### <span data-ttu-id="bec1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec1b-113">-DefaultProfile</span></span>
<span data-ttu-id="bec1b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bec1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec1b-115">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="bec1b-115">-GroupName</span></span>
<span data-ttu-id="bec1b-116">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="bec1b-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec1b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bec1b-117">-InputObject</span></span>
<span data-ttu-id="bec1b-118">Объект input из вызова Get</span><span class="sxs-lookup"><span data-stu-id="bec1b-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec1b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec1b-119">-PassThru</span></span>
<span data-ttu-id="bec1b-120">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="bec1b-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="bec1b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec1b-121">-Confirm</span></span>
<span data-ttu-id="bec1b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bec1b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec1b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec1b-123">-WhatIf</span></span>
<span data-ttu-id="bec1b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bec1b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec1b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bec1b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec1b-126">CommonParameters</span></span>
<span data-ttu-id="bec1b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bec1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec1b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec1b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bec1b-129">INPUTS</span></span>

### <span data-ttu-id="bec1b-130">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="bec1b-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="bec1b-131">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bec1b-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bec1b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec1b-132">OUTPUTS</span></span>

### <span data-ttu-id="bec1b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bec1b-133">System.Boolean</span></span>

## <span data-ttu-id="bec1b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bec1b-134">NOTES</span></span>

## <span data-ttu-id="bec1b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bec1b-135">RELATED LINKS</span></span>
