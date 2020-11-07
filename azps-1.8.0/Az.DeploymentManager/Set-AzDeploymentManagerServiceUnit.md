---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3509212801aaeda9926b7f441e0aae7e17f8cbb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730969"
---
# <span data-ttu-id="3221d-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3221d-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="3221d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3221d-102">SYNOPSIS</span></span>
<span data-ttu-id="3221d-103">Обновляет модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="3221d-103">Updates the service unit.</span></span>

## <span data-ttu-id="3221d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3221d-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3221d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3221d-105">DESCRIPTION</span></span>
<span data-ttu-id="3221d-106">Командлет **Set-AzDeploymentManagerServiceUnit** обновляет модуль обслуживания с помощью указанного объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="3221d-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="3221d-107">Командлет возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="3221d-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="3221d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3221d-108">EXAMPLES</span></span>

### <span data-ttu-id="3221d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3221d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="3221d-110">Эта команда обновляет единицу обслуживания, чье имя, имя службы, имя и группа ресурсов службы совпадают с $serviceUnitObject свойствами Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="3221d-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="3221d-111">Команда возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="3221d-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="3221d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3221d-112">PARAMETERS</span></span>

### <span data-ttu-id="3221d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3221d-113">-DefaultProfile</span></span>
<span data-ttu-id="3221d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3221d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3221d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3221d-115">-InputObject</span></span>
<span data-ttu-id="3221d-116">Объект сервисной единицы.</span><span class="sxs-lookup"><span data-stu-id="3221d-116">The service unit object.</span></span>

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

### <span data-ttu-id="3221d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3221d-117">-Confirm</span></span>
<span data-ttu-id="3221d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3221d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3221d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3221d-119">-WhatIf</span></span>
<span data-ttu-id="3221d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3221d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3221d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3221d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3221d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3221d-122">CommonParameters</span></span>
<span data-ttu-id="3221d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3221d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3221d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3221d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3221d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3221d-125">INPUTS</span></span>

### <span data-ttu-id="3221d-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="3221d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="3221d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3221d-127">OUTPUTS</span></span>

### <span data-ttu-id="3221d-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="3221d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="3221d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="3221d-129">NOTES</span></span>

## <span data-ttu-id="3221d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3221d-130">RELATED LINKS</span></span>
