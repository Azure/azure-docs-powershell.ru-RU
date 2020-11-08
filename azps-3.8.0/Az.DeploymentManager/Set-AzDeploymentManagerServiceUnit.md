---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074363"
---
# <span data-ttu-id="cfe4c-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cfe4c-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="cfe4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfe4c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe4c-103">Обновляет модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-103">Updates the service unit.</span></span>

## <span data-ttu-id="cfe4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfe4c-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfe4c-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe4c-106">Командлет **Set-AzDeploymentManagerServiceUnit** обновляет модуль обслуживания с помощью указанного объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="cfe4c-107">Командлет возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="cfe4c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfe4c-108">EXAMPLES</span></span>

### <span data-ttu-id="cfe4c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfe4c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="cfe4c-110">Эта команда обновляет единицу обслуживания, чье имя, имя службы, имя и группа ресурсов службы совпадают с $serviceUnitObject свойствами Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="cfe4c-111">Команда возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="cfe4c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfe4c-112">PARAMETERS</span></span>

### <span data-ttu-id="cfe4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe4c-113">-DefaultProfile</span></span>
<span data-ttu-id="cfe4c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe4c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfe4c-115">-InputObject</span></span>
<span data-ttu-id="cfe4c-116">Объект сервисной единицы.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-116">The service unit object.</span></span>

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

### <span data-ttu-id="cfe4c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfe4c-117">-Confirm</span></span>
<span data-ttu-id="cfe4c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe4c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe4c-119">-WhatIf</span></span>
<span data-ttu-id="cfe4c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe4c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe4c-122">CommonParameters</span></span>
<span data-ttu-id="cfe4c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfe4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe4c-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfe4c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe4c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfe4c-125">INPUTS</span></span>

### <span data-ttu-id="cfe4c-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cfe4c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cfe4c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfe4c-127">OUTPUTS</span></span>

### <span data-ttu-id="cfe4c-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cfe4c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cfe4c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfe4c-129">NOTES</span></span>

## <span data-ttu-id="cfe4c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfe4c-130">RELATED LINKS</span></span>
