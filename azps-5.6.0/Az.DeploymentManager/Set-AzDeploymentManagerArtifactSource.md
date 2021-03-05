---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980595"
---
# <span data-ttu-id="b0770-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0770-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b0770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0770-102">SYNOPSIS</span></span>
<span data-ttu-id="b0770-103">Обновляет источник артефактов.</span><span class="sxs-lookup"><span data-stu-id="b0770-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="b0770-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0770-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0770-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0770-105">DESCRIPTION</span></span>
<span data-ttu-id="b0770-106">С **помощью cmdlet Set-AzDeploymentManagerArtifactSource** источник артефакта обновляется с помощью указанного объекта-источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="b0770-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="b0770-107">Этот cmdlet возвращает обновленный объект ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="b0770-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="b0770-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0770-108">EXAMPLES</span></span>

### <span data-ttu-id="b0770-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0770-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b0770-110">Эта команда обновляет источник артефакта, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b0770-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="b0770-111">Источник артефакта будет обновляться с емкими свойствами, задами в $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="b0770-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="b0770-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0770-112">PARAMETERS</span></span>

### <span data-ttu-id="b0770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0770-113">-DefaultProfile</span></span>
<span data-ttu-id="b0770-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0770-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0770-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0770-115">-InputObject</span></span>
<span data-ttu-id="b0770-116">Исходный объект артефакта.</span><span class="sxs-lookup"><span data-stu-id="b0770-116">The artifact source object.</span></span>

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

### <span data-ttu-id="b0770-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0770-117">-Confirm</span></span>
<span data-ttu-id="b0770-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b0770-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0770-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0770-119">-WhatIf</span></span>
<span data-ttu-id="b0770-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0770-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0770-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0770-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0770-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0770-122">CommonParameters</span></span>
<span data-ttu-id="b0770-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0770-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0770-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0770-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0770-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0770-125">INPUTS</span></span>

### <span data-ttu-id="b0770-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0770-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b0770-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0770-127">OUTPUTS</span></span>

### <span data-ttu-id="b0770-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b0770-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b0770-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0770-129">NOTES</span></span>

## <span data-ttu-id="b0770-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0770-130">RELATED LINKS</span></span>
