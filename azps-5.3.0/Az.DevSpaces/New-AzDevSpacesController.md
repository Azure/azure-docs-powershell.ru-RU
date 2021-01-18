---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506350"
---
# <span data-ttu-id="9109b-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="9109b-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="9109b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9109b-102">SYNOPSIS</span></span>
<span data-ttu-id="9109b-103">Создайте новый контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="9109b-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9109b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9109b-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9109b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9109b-105">DESCRIPTION</span></span>
<span data-ttu-id="9109b-106">Создайте новый контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="9109b-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="9109b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9109b-107">EXAMPLES</span></span>

### <span data-ttu-id="9109b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9109b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="9109b-109">Создайте контроллер DevSpaces в группе ресурсов devSpaceResourceGroup с именем devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="9109b-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="9109b-110">Используйте кластер clusterName в качестве целевого для этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="9109b-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="9109b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9109b-111">PARAMETERS</span></span>

### <span data-ttu-id="9109b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9109b-112">-AsJob</span></span>
<span data-ttu-id="9109b-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9109b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9109b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9109b-114">-DefaultProfile</span></span>
<span data-ttu-id="9109b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9109b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9109b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9109b-116">-Name</span></span>
<span data-ttu-id="9109b-117">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="9109b-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="9109b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9109b-118">-ResourceGroupName</span></span>
<span data-ttu-id="9109b-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9109b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9109b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="9109b-120">-Tag</span></span>
<span data-ttu-id="9109b-121">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="9109b-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="9109b-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="9109b-122">-TargetClusterName</span></span>
<span data-ttu-id="9109b-123">Название целевого кластера.</span><span class="sxs-lookup"><span data-stu-id="9109b-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="9109b-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9109b-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="9109b-125">Имя целевой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9109b-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="9109b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9109b-126">-Confirm</span></span>
<span data-ttu-id="9109b-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9109b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9109b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9109b-128">-WhatIf</span></span>
<span data-ttu-id="9109b-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9109b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9109b-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9109b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9109b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9109b-131">CommonParameters</span></span>
<span data-ttu-id="9109b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9109b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9109b-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9109b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9109b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9109b-134">INPUTS</span></span>

### <span data-ttu-id="9109b-135">Нет</span><span class="sxs-lookup"><span data-stu-id="9109b-135">None</span></span>

## <span data-ttu-id="9109b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9109b-136">OUTPUTS</span></span>

### <span data-ttu-id="9109b-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="9109b-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="9109b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9109b-138">NOTES</span></span>

## <span data-ttu-id="9109b-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9109b-139">RELATED LINKS</span></span>
