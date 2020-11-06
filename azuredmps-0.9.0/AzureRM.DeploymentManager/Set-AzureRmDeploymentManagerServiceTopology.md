---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: 6387e5a2938bdef99e4aea5e93248a0ecf8e8da7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556416"
---
# <span data-ttu-id="406cd-101">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="406cd-101">Set-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="406cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="406cd-102">SYNOPSIS</span></span>
<span data-ttu-id="406cd-103">Обновляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="406cd-103">Updates the service topology.</span></span>

## <span data-ttu-id="406cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="406cd-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="406cd-105">DESCRIPTION</span></span>
<span data-ttu-id="406cd-106">Командлет **Set-AzureRmDeploymentManagerServiceTopology** обновляет топологию службы с указанным объектом топологии службы.</span><span class="sxs-lookup"><span data-stu-id="406cd-106">The **Set-AzureRmDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="406cd-107">Командлет возвращает обновленный объект Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="406cd-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="406cd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="406cd-108">EXAMPLES</span></span>

### <span data-ttu-id="406cd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="406cd-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="406cd-110">Эта команда обновляет топологию службы, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="406cd-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="406cd-111">Команда возвращает обновленный объект топологии службы.</span><span class="sxs-lookup"><span data-stu-id="406cd-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="406cd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="406cd-112">PARAMETERS</span></span>

### <span data-ttu-id="406cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406cd-113">-DefaultProfile</span></span>
<span data-ttu-id="406cd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="406cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406cd-115">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="406cd-115">-ServiceTopology</span></span>
<span data-ttu-id="406cd-116">Объект Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="406cd-116">The service topology object.</span></span>

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

### <span data-ttu-id="406cd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="406cd-117">-Confirm</span></span>
<span data-ttu-id="406cd-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="406cd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406cd-119">-WhatIf</span></span>
<span data-ttu-id="406cd-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="406cd-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="406cd-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="406cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406cd-122">CommonParameters</span></span>
<span data-ttu-id="406cd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="406cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406cd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406cd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="406cd-125">INPUTS</span></span>

### <span data-ttu-id="406cd-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="406cd-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="406cd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="406cd-127">OUTPUTS</span></span>

### <span data-ttu-id="406cd-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="406cd-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="406cd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="406cd-129">NOTES</span></span>

## <span data-ttu-id="406cd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="406cd-130">RELATED LINKS</span></span>

[<span data-ttu-id="406cd-131">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="406cd-131">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="406cd-132">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="406cd-132">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="406cd-133">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="406cd-133">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)