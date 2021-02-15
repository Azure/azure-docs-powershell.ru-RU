---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230569"
---
# <span data-ttu-id="ffccc-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ffccc-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ffccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffccc-102">SYNOPSIS</span></span>
<span data-ttu-id="ffccc-103">Обновляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="ffccc-103">Updates the service topology.</span></span>

## <span data-ttu-id="ffccc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffccc-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffccc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffccc-105">DESCRIPTION</span></span>
<span data-ttu-id="ffccc-106">**Cmdlet Set-AzDeploymentManagerServiceTopology** обновляет топологию службы с помощью указанного объекта топологии службы.</span><span class="sxs-lookup"><span data-stu-id="ffccc-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="ffccc-107">Cmdlet возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="ffccc-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="ffccc-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffccc-108">EXAMPLES</span></span>

### <span data-ttu-id="ffccc-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ffccc-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="ffccc-110">Эта команда обновляет топологию службы, имя и группа ресурсов которой соответствуют свойствам Name и ResourceGroupName $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="ffccc-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="ffccc-111">Команда возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="ffccc-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="ffccc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffccc-112">PARAMETERS</span></span>

### <span data-ttu-id="ffccc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffccc-113">-DefaultProfile</span></span>
<span data-ttu-id="ffccc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffccc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffccc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffccc-115">-InputObject</span></span>
<span data-ttu-id="ffccc-116">Объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="ffccc-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffccc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffccc-117">-Confirm</span></span>
<span data-ttu-id="ffccc-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffccc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffccc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffccc-119">-WhatIf</span></span>
<span data-ttu-id="ffccc-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffccc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffccc-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ffccc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffccc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffccc-122">CommonParameters</span></span>
<span data-ttu-id="ffccc-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffccc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffccc-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffccc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffccc-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffccc-125">INPUTS</span></span>

### <span data-ttu-id="ffccc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ffccc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ffccc-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffccc-127">OUTPUTS</span></span>

### <span data-ttu-id="ffccc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ffccc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ffccc-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffccc-129">NOTES</span></span>

## <span data-ttu-id="ffccc-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffccc-130">RELATED LINKS</span></span>
