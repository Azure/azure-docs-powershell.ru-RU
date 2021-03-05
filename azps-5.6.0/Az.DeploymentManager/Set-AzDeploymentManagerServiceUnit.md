---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 24c682faf725fd53e3b78e85c316318300ecbb62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962088"
---
# <span data-ttu-id="91e94-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="91e94-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="91e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e94-102">SYNOPSIS</span></span>
<span data-ttu-id="91e94-103">Обновляет единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="91e94-103">Updates the service unit.</span></span>

## <span data-ttu-id="91e94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91e94-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e94-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e94-105">DESCRIPTION</span></span>
<span data-ttu-id="91e94-106">**Cmdlet Set-AzDeploymentManagerServiceUnit** обновляет единицу обслуживания с помощью указанного объекта единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="91e94-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="91e94-107">Cmdlet возвращает обновленный объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="91e94-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="91e94-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91e94-108">EXAMPLES</span></span>

### <span data-ttu-id="91e94-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91e94-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="91e94-110">Эта команда обновляет единицу службы, имя которой, имя службы, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceName, ServiceTopologyName и ResourceGroupName $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="91e94-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="91e94-111">Команда возвращает обновленный объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="91e94-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="91e94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e94-112">PARAMETERS</span></span>

### <span data-ttu-id="91e94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e94-113">-DefaultProfile</span></span>
<span data-ttu-id="91e94-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91e94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e94-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91e94-115">-InputObject</span></span>
<span data-ttu-id="91e94-116">Объект единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="91e94-116">The service unit object.</span></span>

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

### <span data-ttu-id="91e94-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91e94-117">-Confirm</span></span>
<span data-ttu-id="91e94-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e94-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e94-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e94-119">-WhatIf</span></span>
<span data-ttu-id="91e94-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e94-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e94-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91e94-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e94-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e94-122">CommonParameters</span></span>
<span data-ttu-id="91e94-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e94-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e94-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91e94-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e94-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91e94-125">INPUTS</span></span>

### <span data-ttu-id="91e94-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="91e94-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="91e94-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91e94-127">OUTPUTS</span></span>

### <span data-ttu-id="91e94-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="91e94-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="91e94-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91e94-129">NOTES</span></span>

## <span data-ttu-id="91e94-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91e94-130">RELATED LINKS</span></span>
