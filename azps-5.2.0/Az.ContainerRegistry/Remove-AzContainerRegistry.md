---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: d36e362f1782e3566bc0d2febd65aebd4c68220d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408628"
---
# <span data-ttu-id="34083-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34083-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="34083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34083-102">SYNOPSIS</span></span>
<span data-ttu-id="34083-103">Удаляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="34083-103">Removes a container registry.</span></span>

## <span data-ttu-id="34083-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34083-104">SYNTAX</span></span>

### <span data-ttu-id="34083-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34083-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34083-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34083-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34083-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34083-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34083-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34083-108">DESCRIPTION</span></span>
<span data-ttu-id="34083-109">С Remove-AzContainerRegistry-за этого реестр контейнера удаляется.</span><span class="sxs-lookup"><span data-stu-id="34083-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="34083-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34083-110">EXAMPLES</span></span>

### <span data-ttu-id="34083-111">Пример 1. Удаление указанного реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="34083-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="34083-112">Эта команда удаляет указанный реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="34083-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="34083-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34083-113">PARAMETERS</span></span>

### <span data-ttu-id="34083-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34083-114">-DefaultProfile</span></span>
<span data-ttu-id="34083-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34083-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34083-116">-Name</span><span class="sxs-lookup"><span data-stu-id="34083-116">-Name</span></span>
<span data-ttu-id="34083-117">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="34083-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="34083-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34083-118">-PassThru</span></span>
<span data-ttu-id="34083-119">Указывает на то, что этот cmdlet возвращает истина, если удаление было успешно.</span><span class="sxs-lookup"><span data-stu-id="34083-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="34083-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="34083-120">-Registry</span></span>
<span data-ttu-id="34083-121">Объект Container Registry.</span><span class="sxs-lookup"><span data-stu-id="34083-121">Container Registry Object.</span></span>

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

### <span data-ttu-id="34083-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34083-122">-ResourceGroupName</span></span>
<span data-ttu-id="34083-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34083-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="34083-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34083-124">-ResourceId</span></span>
<span data-ttu-id="34083-125">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="34083-125">The container registry resource id</span></span>

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

### <span data-ttu-id="34083-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34083-126">-Confirm</span></span>
<span data-ttu-id="34083-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34083-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34083-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34083-128">-WhatIf</span></span>
<span data-ttu-id="34083-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34083-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34083-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34083-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34083-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34083-131">CommonParameters</span></span>
<span data-ttu-id="34083-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34083-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34083-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34083-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34083-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34083-134">INPUTS</span></span>

### <span data-ttu-id="34083-135">System.String</span><span class="sxs-lookup"><span data-stu-id="34083-135">System.String</span></span>

## <span data-ttu-id="34083-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34083-136">OUTPUTS</span></span>

### <span data-ttu-id="34083-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34083-137">System.Boolean</span></span>

## <span data-ttu-id="34083-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34083-138">NOTES</span></span>

## <span data-ttu-id="34083-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34083-139">RELATED LINKS</span></span>

[<span data-ttu-id="34083-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34083-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="34083-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34083-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="34083-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34083-142">Update-AzContainerRegistry</span></span>]()

