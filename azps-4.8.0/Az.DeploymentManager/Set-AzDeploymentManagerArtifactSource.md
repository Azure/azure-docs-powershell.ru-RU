---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244557"
---
# <span data-ttu-id="d4263-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d4263-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d4263-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4263-102">SYNOPSIS</span></span>
<span data-ttu-id="d4263-103">Обновляет источник артефактов.</span><span class="sxs-lookup"><span data-stu-id="d4263-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="d4263-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4263-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4263-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4263-105">DESCRIPTION</span></span>
<span data-ttu-id="d4263-106">Командлет **Set-AzDeploymentManagerArtifactSource** обновляет источник артефакта с указанным объектом источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="d4263-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="d4263-107">Командлет возвращает обновленный объект ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="d4263-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="d4263-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4263-108">EXAMPLES</span></span>

### <span data-ttu-id="d4263-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4263-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="d4263-110">Эта команда обновляет источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="d4263-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="d4263-111">Источник артефактов обновится до свойств, заданных в $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="d4263-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="d4263-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4263-112">PARAMETERS</span></span>

### <span data-ttu-id="d4263-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4263-113">-DefaultProfile</span></span>
<span data-ttu-id="d4263-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4263-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4263-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4263-115">-InputObject</span></span>
<span data-ttu-id="d4263-116">Объект источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="d4263-116">The artifact source object.</span></span>

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

### <span data-ttu-id="d4263-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4263-117">-Confirm</span></span>
<span data-ttu-id="d4263-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4263-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4263-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4263-119">-WhatIf</span></span>
<span data-ttu-id="d4263-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4263-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4263-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4263-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4263-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4263-122">CommonParameters</span></span>
<span data-ttu-id="d4263-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4263-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4263-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4263-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4263-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4263-125">INPUTS</span></span>

### <span data-ttu-id="d4263-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d4263-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d4263-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4263-127">OUTPUTS</span></span>

### <span data-ttu-id="d4263-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d4263-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d4263-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4263-129">NOTES</span></span>

## <span data-ttu-id="d4263-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4263-130">RELATED LINKS</span></span>
