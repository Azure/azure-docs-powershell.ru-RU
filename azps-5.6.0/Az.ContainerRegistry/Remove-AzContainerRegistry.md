---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: 49da6e1efbd1bb0e6b0ac4dc693d51fe5b58bfac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015384"
---
# <span data-ttu-id="29a4d-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29a4d-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="29a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="29a4d-103">Удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="29a4d-103">Removes a container registry.</span></span>

## <span data-ttu-id="29a4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29a4d-104">SYNTAX</span></span>

### <span data-ttu-id="29a4d-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29a4d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29a4d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29a4d-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29a4d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29a4d-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29a4d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29a4d-108">DESCRIPTION</span></span>
<span data-ttu-id="29a4d-109">С Remove-AzContainerRegistry-за этого реестр контейнера удаляется.</span><span class="sxs-lookup"><span data-stu-id="29a4d-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="29a4d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29a4d-110">EXAMPLES</span></span>

### <span data-ttu-id="29a4d-111">Пример 1. Удаление указанного реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="29a4d-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="29a4d-112">Эта команда удаляет указанный реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="29a4d-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="29a4d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29a4d-113">PARAMETERS</span></span>

### <span data-ttu-id="29a4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a4d-114">-DefaultProfile</span></span>
<span data-ttu-id="29a4d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="29a4d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29a4d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="29a4d-116">-Name</span></span>
<span data-ttu-id="29a4d-117">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="29a4d-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29a4d-118">-PassThru</span></span>
<span data-ttu-id="29a4d-119">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="29a4d-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="29a4d-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="29a4d-120">-Registry</span></span>
<span data-ttu-id="29a4d-121">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="29a4d-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="29a4d-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29a4d-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29a4d-124">-ResourceId</span></span>
<span data-ttu-id="29a4d-125">ИД ресурса контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="29a4d-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29a4d-126">-Confirm</span></span>
<span data-ttu-id="29a4d-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29a4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29a4d-128">-WhatIf</span></span>
<span data-ttu-id="29a4d-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29a4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29a4d-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29a4d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a4d-131">CommonParameters</span></span>
<span data-ttu-id="29a4d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a4d-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29a4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a4d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29a4d-134">INPUTS</span></span>

### <span data-ttu-id="29a4d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="29a4d-135">System.String</span></span>

## <span data-ttu-id="29a4d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29a4d-136">OUTPUTS</span></span>

### <span data-ttu-id="29a4d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29a4d-137">System.Boolean</span></span>

## <span data-ttu-id="29a4d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29a4d-138">NOTES</span></span>

## <span data-ttu-id="29a4d-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29a4d-139">RELATED LINKS</span></span>

[<span data-ttu-id="29a4d-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29a4d-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="29a4d-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29a4d-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="29a4d-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="29a4d-142">Update-AzContainerRegistry</span></span>]()

