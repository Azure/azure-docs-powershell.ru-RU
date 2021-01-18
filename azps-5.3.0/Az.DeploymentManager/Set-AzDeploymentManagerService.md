---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507589"
---
# <span data-ttu-id="324c8-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="324c8-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="324c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="324c8-102">SYNOPSIS</span></span>
<span data-ttu-id="324c8-103">Обновляет службу.</span><span class="sxs-lookup"><span data-stu-id="324c8-103">Updates the service.</span></span>

## <span data-ttu-id="324c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="324c8-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="324c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="324c8-105">DESCRIPTION</span></span>
<span data-ttu-id="324c8-106">**Cmdlet Set-AzDeploymentManagerService** обновляет службу с помощью указанного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="324c8-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="324c8-107">Cmdlet возвращает обновленный объект службы.</span><span class="sxs-lookup"><span data-stu-id="324c8-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="324c8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="324c8-108">EXAMPLES</span></span>

### <span data-ttu-id="324c8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="324c8-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="324c8-110">Эта команда обновляет службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="324c8-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="324c8-111">Служба будет обновлена в свойствах, задамые в $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="324c8-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="324c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="324c8-112">PARAMETERS</span></span>

### <span data-ttu-id="324c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324c8-113">-DefaultProfile</span></span>
<span data-ttu-id="324c8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="324c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="324c8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="324c8-115">-InputObject</span></span>
<span data-ttu-id="324c8-116">Объект-служба.</span><span class="sxs-lookup"><span data-stu-id="324c8-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="324c8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="324c8-117">-Confirm</span></span>
<span data-ttu-id="324c8-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="324c8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="324c8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324c8-119">-WhatIf</span></span>
<span data-ttu-id="324c8-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="324c8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="324c8-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="324c8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="324c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324c8-122">CommonParameters</span></span>
<span data-ttu-id="324c8-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="324c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324c8-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="324c8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324c8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="324c8-125">INPUTS</span></span>

### <span data-ttu-id="324c8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="324c8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="324c8-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="324c8-127">OUTPUTS</span></span>

### <span data-ttu-id="324c8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="324c8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="324c8-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="324c8-129">NOTES</span></span>

## <span data-ttu-id="324c8-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="324c8-130">RELATED LINKS</span></span>
