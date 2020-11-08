---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074362"
---
# <span data-ttu-id="b8859-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b8859-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="b8859-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8859-102">SYNOPSIS</span></span>
<span data-ttu-id="b8859-103">Обновляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="b8859-103">Updates the service topology.</span></span>

## <span data-ttu-id="b8859-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8859-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8859-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8859-105">DESCRIPTION</span></span>
<span data-ttu-id="b8859-106">Командлет **Set-AzDeploymentManagerServiceTopology** обновляет топологию службы с указанным объектом топологии службы.</span><span class="sxs-lookup"><span data-stu-id="b8859-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="b8859-107">Командлет возвращает обновленный объект Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="b8859-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="b8859-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8859-108">EXAMPLES</span></span>

### <span data-ttu-id="b8859-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8859-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="b8859-110">Эта команда обновляет топологию службы, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b8859-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="b8859-111">Команда возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="b8859-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="b8859-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8859-112">PARAMETERS</span></span>

### <span data-ttu-id="b8859-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8859-113">-DefaultProfile</span></span>
<span data-ttu-id="b8859-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8859-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8859-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8859-115">-InputObject</span></span>
<span data-ttu-id="b8859-116">Объект Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="b8859-116">The service topology object.</span></span>

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

### <span data-ttu-id="b8859-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8859-117">-Confirm</span></span>
<span data-ttu-id="b8859-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8859-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8859-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8859-119">-WhatIf</span></span>
<span data-ttu-id="b8859-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8859-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8859-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8859-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8859-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8859-122">CommonParameters</span></span>
<span data-ttu-id="b8859-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8859-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8859-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8859-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8859-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8859-125">INPUTS</span></span>

### <span data-ttu-id="b8859-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="b8859-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="b8859-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8859-127">OUTPUTS</span></span>

### <span data-ttu-id="b8859-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="b8859-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="b8859-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8859-129">NOTES</span></span>

## <span data-ttu-id="b8859-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8859-130">RELATED LINKS</span></span>
