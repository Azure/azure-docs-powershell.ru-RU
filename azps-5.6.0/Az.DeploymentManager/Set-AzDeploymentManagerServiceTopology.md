---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7e3ed99abe5fb7a679506571d7d734cad02084d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966248"
---
# <span data-ttu-id="a8b73-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a8b73-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="a8b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b73-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b73-103">Обновляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="a8b73-103">Updates the service topology.</span></span>

## <span data-ttu-id="a8b73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8b73-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b73-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8b73-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b73-106">**Cmdlet Set-AzDeploymentManagerServiceTopology** обновляет топологию службы с помощью указанного объекта топологии службы.</span><span class="sxs-lookup"><span data-stu-id="a8b73-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="a8b73-107">Cmdlet возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="a8b73-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="a8b73-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8b73-108">EXAMPLES</span></span>

### <span data-ttu-id="a8b73-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8b73-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="a8b73-110">Эта команда обновляет топологию службы, имя и группа ресурсов которой соответствуют свойствам Name и ResourceGroupName $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="a8b73-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="a8b73-111">Команда возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="a8b73-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="a8b73-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8b73-112">PARAMETERS</span></span>

### <span data-ttu-id="a8b73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b73-113">-DefaultProfile</span></span>
<span data-ttu-id="a8b73-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b73-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8b73-115">-InputObject</span></span>
<span data-ttu-id="a8b73-116">Объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="a8b73-116">The service topology object.</span></span>

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

### <span data-ttu-id="a8b73-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8b73-117">-Confirm</span></span>
<span data-ttu-id="a8b73-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b73-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b73-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b73-119">-WhatIf</span></span>
<span data-ttu-id="a8b73-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b73-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b73-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8b73-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b73-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b73-122">CommonParameters</span></span>
<span data-ttu-id="a8b73-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b73-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b73-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8b73-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b73-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8b73-125">INPUTS</span></span>

### <span data-ttu-id="a8b73-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a8b73-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a8b73-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8b73-127">OUTPUTS</span></span>

### <span data-ttu-id="a8b73-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a8b73-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a8b73-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8b73-129">NOTES</span></span>

## <span data-ttu-id="a8b73-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8b73-130">RELATED LINKS</span></span>
