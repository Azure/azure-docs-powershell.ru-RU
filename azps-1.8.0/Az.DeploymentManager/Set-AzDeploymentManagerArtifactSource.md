---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 32e5293f7c5bb62711a6510c590aa1ba7f4229b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730975"
---
# <span data-ttu-id="8964c-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="8964c-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="8964c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8964c-102">SYNOPSIS</span></span>
<span data-ttu-id="8964c-103">Обновляет источник артефактов.</span><span class="sxs-lookup"><span data-stu-id="8964c-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="8964c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8964c-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8964c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8964c-105">DESCRIPTION</span></span>
<span data-ttu-id="8964c-106">Командлет **Set-AzDeploymentManagerArtifactSource** обновляет источник артефакта с указанным объектом источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="8964c-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="8964c-107">Командлет возвращает обновленный объект ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="8964c-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="8964c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8964c-108">EXAMPLES</span></span>

### <span data-ttu-id="8964c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8964c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="8964c-110">Эта команда обновляет источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="8964c-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="8964c-111">Источник артефактов обновится до свойств, заданных в $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="8964c-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="8964c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8964c-112">PARAMETERS</span></span>

### <span data-ttu-id="8964c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8964c-113">-DefaultProfile</span></span>
<span data-ttu-id="8964c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8964c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8964c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8964c-115">-InputObject</span></span>
<span data-ttu-id="8964c-116">Объект источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="8964c-116">The artifact source object.</span></span>

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

### <span data-ttu-id="8964c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8964c-117">-Confirm</span></span>
<span data-ttu-id="8964c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8964c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8964c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8964c-119">-WhatIf</span></span>
<span data-ttu-id="8964c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8964c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8964c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8964c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8964c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8964c-122">CommonParameters</span></span>
<span data-ttu-id="8964c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8964c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8964c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8964c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8964c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8964c-125">INPUTS</span></span>

### <span data-ttu-id="8964c-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="8964c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="8964c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8964c-127">OUTPUTS</span></span>

### <span data-ttu-id="8964c-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="8964c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="8964c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8964c-129">NOTES</span></span>

## <span data-ttu-id="8964c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8964c-130">RELATED LINKS</span></span>
