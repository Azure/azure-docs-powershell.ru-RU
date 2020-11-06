---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555568"
---
# <span data-ttu-id="bc342-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="bc342-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc342-102">SYNOPSIS</span></span>
<span data-ttu-id="bc342-103">Обновляет источник артефакта.</span><span class="sxs-lookup"><span data-stu-id="bc342-103">Updates an artifact source.</span></span>

## <span data-ttu-id="bc342-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc342-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc342-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc342-105">DESCRIPTION</span></span>
<span data-ttu-id="bc342-106">Командлет **Set-AzureRmDeploymentManagerArtifactSource** обновляет источник артефакта с указанным объектом источника артефакта.</span><span class="sxs-lookup"><span data-stu-id="bc342-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="bc342-107">Командлет возвращает обновленный объект ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="bc342-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="bc342-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc342-108">EXAMPLES</span></span>

### <span data-ttu-id="bc342-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc342-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="bc342-110">Эта команда обновляет источник артефакта, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $artifactSourceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="bc342-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="bc342-111">Источник артефактов обновится до свойств, заданных в $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="bc342-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="bc342-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc342-112">PARAMETERS</span></span>

### <span data-ttu-id="bc342-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-113">-ArtifactSource</span></span>
<span data-ttu-id="bc342-114">Объект источника артефактов.</span><span class="sxs-lookup"><span data-stu-id="bc342-114">The artifact source object.</span></span>

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

### <span data-ttu-id="bc342-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc342-115">-DefaultProfile</span></span>
<span data-ttu-id="bc342-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc342-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc342-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc342-117">-Confirm</span></span>
<span data-ttu-id="bc342-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc342-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc342-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc342-119">-WhatIf</span></span>
<span data-ttu-id="bc342-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc342-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc342-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc342-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc342-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc342-122">CommonParameters</span></span>
<span data-ttu-id="bc342-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc342-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc342-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc342-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc342-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc342-125">INPUTS</span></span>

### <span data-ttu-id="bc342-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="bc342-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc342-127">OUTPUTS</span></span>

### <span data-ttu-id="bc342-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="bc342-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc342-129">NOTES</span></span>

## <span data-ttu-id="bc342-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc342-130">RELATED LINKS</span></span>

[<span data-ttu-id="bc342-131">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="bc342-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="bc342-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc342-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)