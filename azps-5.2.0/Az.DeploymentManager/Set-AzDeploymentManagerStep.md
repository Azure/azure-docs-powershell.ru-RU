---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393508"
---
# <span data-ttu-id="05ec3-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="05ec3-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="05ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="05ec3-103">Обновляет шаг.</span><span class="sxs-lookup"><span data-stu-id="05ec3-103">Updates the step.</span></span>

## <span data-ttu-id="05ec3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05ec3-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ec3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="05ec3-106">**Cmdlet Set-AzDeploymentManagerStep** обновляет шаг с помощью указанного объекта шага.</span><span class="sxs-lookup"><span data-stu-id="05ec3-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="05ec3-107">Cmdlet возвращает обновленный шаг объекта.</span><span class="sxs-lookup"><span data-stu-id="05ec3-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="05ec3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05ec3-108">EXAMPLES</span></span>

### <span data-ttu-id="05ec3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05ec3-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="05ec3-110">Эта команда обновляет шаг, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="05ec3-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="05ec3-111">Шаг будет обновляться в свойствах, задамые в $stepObject.</span><span class="sxs-lookup"><span data-stu-id="05ec3-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="05ec3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05ec3-112">PARAMETERS</span></span>

### <span data-ttu-id="05ec3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ec3-113">-DefaultProfile</span></span>
<span data-ttu-id="05ec3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05ec3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ec3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05ec3-115">-InputObject</span></span>
<span data-ttu-id="05ec3-116">Объект шага.</span><span class="sxs-lookup"><span data-stu-id="05ec3-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ec3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05ec3-117">-Confirm</span></span>
<span data-ttu-id="05ec3-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="05ec3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ec3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ec3-119">-WhatIf</span></span>
<span data-ttu-id="05ec3-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ec3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ec3-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="05ec3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ec3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ec3-122">CommonParameters</span></span>
<span data-ttu-id="05ec3-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ec3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ec3-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05ec3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ec3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05ec3-125">INPUTS</span></span>

### <span data-ttu-id="05ec3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="05ec3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="05ec3-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05ec3-127">OUTPUTS</span></span>

### <span data-ttu-id="05ec3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="05ec3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="05ec3-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05ec3-129">NOTES</span></span>

## <span data-ttu-id="05ec3-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05ec3-130">RELATED LINKS</span></span>
