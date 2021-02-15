---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230577"
---
# <span data-ttu-id="a9c37-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a9c37-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="a9c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c37-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c37-103">Обновляет службу.</span><span class="sxs-lookup"><span data-stu-id="a9c37-103">Updates the service.</span></span>

## <span data-ttu-id="a9c37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9c37-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c37-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c37-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c37-106">**Cmdlet Set-AzDeploymentManagerService** обновляет службу с помощью указанного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="a9c37-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="a9c37-107">Cmdlet возвращает обновленный объект службы.</span><span class="sxs-lookup"><span data-stu-id="a9c37-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="a9c37-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9c37-108">EXAMPLES</span></span>

### <span data-ttu-id="a9c37-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9c37-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="a9c37-110">Эта команда обновляет службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="a9c37-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="a9c37-111">Служба будет обновлена в свойствах, задамые в $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="a9c37-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="a9c37-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9c37-112">PARAMETERS</span></span>

### <span data-ttu-id="a9c37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c37-113">-DefaultProfile</span></span>
<span data-ttu-id="a9c37-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c37-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c37-115">-InputObject</span></span>
<span data-ttu-id="a9c37-116">Объект-служба.</span><span class="sxs-lookup"><span data-stu-id="a9c37-116">The service object.</span></span>

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

### <span data-ttu-id="a9c37-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9c37-117">-Confirm</span></span>
<span data-ttu-id="a9c37-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9c37-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c37-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c37-119">-WhatIf</span></span>
<span data-ttu-id="a9c37-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9c37-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c37-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a9c37-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c37-122">CommonParameters</span></span>
<span data-ttu-id="a9c37-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c37-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c37-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c37-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9c37-125">INPUTS</span></span>

### <span data-ttu-id="a9c37-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a9c37-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a9c37-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9c37-127">OUTPUTS</span></span>

### <span data-ttu-id="a9c37-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a9c37-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a9c37-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9c37-129">NOTES</span></span>

## <span data-ttu-id="a9c37-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9c37-130">RELATED LINKS</span></span>
