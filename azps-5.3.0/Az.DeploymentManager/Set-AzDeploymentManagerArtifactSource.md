---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506384"
---
# <span data-ttu-id="b6033-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b6033-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b6033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6033-102">SYNOPSIS</span></span>
<span data-ttu-id="b6033-103">Обновляет источник артефактов.</span><span class="sxs-lookup"><span data-stu-id="b6033-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="b6033-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6033-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6033-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6033-105">DESCRIPTION</span></span>
<span data-ttu-id="b6033-106">С **помощью cmdlet Set-AzDeploymentManagerArtifactSource** можно обновить источник артефакта с помощью указанного объекта-источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="b6033-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="b6033-107">Этот cmdlet возвращает обновленный объект ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="b6033-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="b6033-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6033-108">EXAMPLES</span></span>

### <span data-ttu-id="b6033-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6033-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b6033-110">Эта команда обновляет источник артефакта, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b6033-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="b6033-111">Источник артефакта будет обновляться в свойствах, задамых в $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="b6033-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="b6033-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6033-112">PARAMETERS</span></span>

### <span data-ttu-id="b6033-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6033-113">-DefaultProfile</span></span>
<span data-ttu-id="b6033-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6033-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6033-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6033-115">-InputObject</span></span>
<span data-ttu-id="b6033-116">Исходный объект артефакта.</span><span class="sxs-lookup"><span data-stu-id="b6033-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6033-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6033-117">-Confirm</span></span>
<span data-ttu-id="b6033-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b6033-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6033-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6033-119">-WhatIf</span></span>
<span data-ttu-id="b6033-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6033-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6033-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6033-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6033-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6033-122">CommonParameters</span></span>
<span data-ttu-id="b6033-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6033-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6033-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6033-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6033-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6033-125">INPUTS</span></span>

### <span data-ttu-id="b6033-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b6033-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b6033-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6033-127">OUTPUTS</span></span>

### <span data-ttu-id="b6033-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b6033-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b6033-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6033-129">NOTES</span></span>

## <span data-ttu-id="b6033-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6033-130">RELATED LINKS</span></span>
