---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312647"
---
# <span data-ttu-id="3b578-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3b578-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="3b578-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b578-102">SYNOPSIS</span></span>
<span data-ttu-id="3b578-103">Обновляет службу.</span><span class="sxs-lookup"><span data-stu-id="3b578-103">Updates the service.</span></span>

## <span data-ttu-id="3b578-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b578-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b578-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b578-105">DESCRIPTION</span></span>
<span data-ttu-id="3b578-106">Командлет **Set-AzDeploymentManagerService** обновляет службу с помощью указанного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="3b578-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="3b578-107">Командлет возвращает обновленный объект службы.</span><span class="sxs-lookup"><span data-stu-id="3b578-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="3b578-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b578-108">EXAMPLES</span></span>

### <span data-ttu-id="3b578-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b578-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="3b578-110">Эта команда обновляет службу, имя которой, имя топологии службы и ResourceGroup, совпадают со свойствами Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="3b578-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="3b578-111">Служба будет обновлена до свойств, заданных в $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3b578-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="3b578-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b578-112">PARAMETERS</span></span>

### <span data-ttu-id="3b578-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b578-113">-DefaultProfile</span></span>
<span data-ttu-id="3b578-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b578-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b578-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b578-115">-InputObject</span></span>
<span data-ttu-id="3b578-116">Объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="3b578-116">The service object.</span></span>

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

### <span data-ttu-id="3b578-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b578-117">-Confirm</span></span>
<span data-ttu-id="3b578-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b578-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b578-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b578-119">-WhatIf</span></span>
<span data-ttu-id="3b578-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b578-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b578-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b578-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b578-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b578-122">CommonParameters</span></span>
<span data-ttu-id="3b578-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b578-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b578-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b578-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b578-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b578-125">INPUTS</span></span>

### <span data-ttu-id="3b578-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3b578-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3b578-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b578-127">OUTPUTS</span></span>

### <span data-ttu-id="3b578-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3b578-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3b578-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b578-129">NOTES</span></span>

## <span data-ttu-id="3b578-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b578-130">RELATED LINKS</span></span>
