---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 0429eebf0425a950bcf093d7659a2d87b3b661f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721093"
---
# <span data-ttu-id="0ab3a-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="0ab3a-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="0ab3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ab3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab3a-103">Создайте новый контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="0ab3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ab3a-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab3a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab3a-106">Создайте новый контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="0ab3a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ab3a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab3a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ab3a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="0ab3a-109">Создайте контроллер DevSpaces в группе resourcegroup devSpaceResourceGroup с именем devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="0ab3a-110">Используйте Cluster имя_кластера в качестве целевого объекта для этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="0ab3a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ab3a-111">PARAMETERS</span></span>

### <span data-ttu-id="0ab3a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ab3a-112">-AsJob</span></span>
<span data-ttu-id="0ab3a-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0ab3a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ab3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab3a-114">-DefaultProfile</span></span>
<span data-ttu-id="0ab3a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab3a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ab3a-116">-Name</span></span>
<span data-ttu-id="0ab3a-117">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab3a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab3a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0ab3a-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab3a-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="0ab3a-120">-Tag</span></span>
<span data-ttu-id="0ab3a-121">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0ab3a-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="0ab3a-122">-TargetClusterName</span></span>
<span data-ttu-id="0ab3a-123">Имя целевого кластера.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab3a-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab3a-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="0ab3a-125">Целевое имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab3a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ab3a-126">-Confirm</span></span>
<span data-ttu-id="0ab3a-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab3a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab3a-128">-WhatIf</span></span>
<span data-ttu-id="0ab3a-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab3a-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab3a-131">CommonParameters</span></span>
<span data-ttu-id="0ab3a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ab3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab3a-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab3a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab3a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ab3a-134">INPUTS</span></span>

### <span data-ttu-id="0ab3a-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="0ab3a-135">None</span></span>

## <span data-ttu-id="0ab3a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab3a-136">OUTPUTS</span></span>

### <span data-ttu-id="0ab3a-137">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="0ab3a-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="0ab3a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ab3a-138">NOTES</span></span>

## <span data-ttu-id="0ab3a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ab3a-139">RELATED LINKS</span></span>
