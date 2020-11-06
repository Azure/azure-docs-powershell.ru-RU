---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555743"
---
# <span data-ttu-id="e597a-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="e597a-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="e597a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e597a-102">SYNOPSIS</span></span>
<span data-ttu-id="e597a-103">Обновляет модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e597a-103">Updates a service unit.</span></span>

## <span data-ttu-id="e597a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e597a-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e597a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e597a-105">DESCRIPTION</span></span>
<span data-ttu-id="e597a-106">Командлет **Set-AzureRmDeploymentManagerServiceUnit** обновляет модуль обслуживания с помощью указанного объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e597a-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="e597a-107">Командлет возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="e597a-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="e597a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e597a-108">EXAMPLES</span></span>

### <span data-ttu-id="e597a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e597a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="e597a-110">Эта команда обновляет единицу обслуживания, чье имя, имя службы, имя и группа ресурсов службы совпадают с $serviceUnitObject свойствами Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="e597a-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="e597a-111">Команда возвращает обновленный объект модуля Service.</span><span class="sxs-lookup"><span data-stu-id="e597a-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="e597a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e597a-112">PARAMETERS</span></span>

### <span data-ttu-id="e597a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e597a-113">-DefaultProfile</span></span>
<span data-ttu-id="e597a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e597a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e597a-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="e597a-115">-ServiceUnit</span></span>
<span data-ttu-id="e597a-116">Объект сервисной единицы.</span><span class="sxs-lookup"><span data-stu-id="e597a-116">The service unit object.</span></span>

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

### <span data-ttu-id="e597a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e597a-117">-Confirm</span></span>
<span data-ttu-id="e597a-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e597a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e597a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e597a-119">-WhatIf</span></span>
<span data-ttu-id="e597a-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e597a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e597a-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e597a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e597a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e597a-122">CommonParameters</span></span>
<span data-ttu-id="e597a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e597a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e597a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e597a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e597a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e597a-125">INPUTS</span></span>

### <span data-ttu-id="e597a-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="e597a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="e597a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e597a-127">OUTPUTS</span></span>

### <span data-ttu-id="e597a-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="e597a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="e597a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e597a-129">NOTES</span></span>

## <span data-ttu-id="e597a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e597a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e597a-131">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="e597a-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="e597a-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="e597a-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="e597a-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="e597a-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)