---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506383"
---
# <span data-ttu-id="cea9e-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cea9e-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="cea9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="cea9e-103">Обновляет единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cea9e-103">Updates the service unit.</span></span>

## <span data-ttu-id="cea9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cea9e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea9e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cea9e-105">DESCRIPTION</span></span>
<span data-ttu-id="cea9e-106">С **помощью cmdlet Set-AzDeploymentManagerServiceUnit** можно обновить единицу обслуживания с помощью указанного объекта единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cea9e-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="cea9e-107">Cmdlet возвращает обновленный объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cea9e-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="cea9e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cea9e-108">EXAMPLES</span></span>

### <span data-ttu-id="cea9e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cea9e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="cea9e-110">Эта команда обновляет единицу службы, имя которой, имя службы, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceName, ServiceTopologyName и ResourceGroupName $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="cea9e-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="cea9e-111">Команда возвращает обновленный объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cea9e-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="cea9e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cea9e-112">PARAMETERS</span></span>

### <span data-ttu-id="cea9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea9e-113">-DefaultProfile</span></span>
<span data-ttu-id="cea9e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cea9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea9e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cea9e-115">-InputObject</span></span>
<span data-ttu-id="cea9e-116">Объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cea9e-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cea9e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cea9e-117">-Confirm</span></span>
<span data-ttu-id="cea9e-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cea9e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea9e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea9e-119">-WhatIf</span></span>
<span data-ttu-id="cea9e-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cea9e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea9e-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cea9e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea9e-122">CommonParameters</span></span>
<span data-ttu-id="cea9e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea9e-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cea9e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea9e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cea9e-125">INPUTS</span></span>

### <span data-ttu-id="cea9e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cea9e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cea9e-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cea9e-127">OUTPUTS</span></span>

### <span data-ttu-id="cea9e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cea9e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cea9e-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cea9e-129">NOTES</span></span>

## <span data-ttu-id="cea9e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cea9e-130">RELATED LINKS</span></span>
