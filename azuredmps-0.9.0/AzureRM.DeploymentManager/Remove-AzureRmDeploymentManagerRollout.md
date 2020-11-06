---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555311"
---
# <span data-ttu-id="de593-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="de593-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="de593-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de593-102">SYNOPSIS</span></span>
<span data-ttu-id="de593-103">Удаление выпуска.</span><span class="sxs-lookup"><span data-stu-id="de593-103">Deletes a rollout.</span></span>

## <span data-ttu-id="de593-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de593-104">SYNTAX</span></span>

### <span data-ttu-id="de593-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de593-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de593-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de593-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de593-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="de593-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de593-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de593-108">DESCRIPTION</span></span>
<span data-ttu-id="de593-109">Командлет **Remove-AzureRmDeploymentManagerRollout** удаляет выпуск в состоянии терминала.</span><span class="sxs-lookup"><span data-stu-id="de593-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="de593-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de593-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="de593-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="de593-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="de593-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de593-112">EXAMPLES</span></span>

### <span data-ttu-id="de593-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de593-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="de593-114">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="de593-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="de593-115">Пример 2: удаление выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="de593-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="de593-116">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="de593-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="de593-117">Пример 3: удаление выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="de593-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="de593-118">Эта команда удаляет выпуску, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName в $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="de593-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="de593-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de593-119">PARAMETERS</span></span>

### <span data-ttu-id="de593-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de593-120">-DefaultProfile</span></span>
<span data-ttu-id="de593-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de593-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de593-122">-Force</span><span class="sxs-lookup"><span data-stu-id="de593-122">-Force</span></span>
<span data-ttu-id="de593-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="de593-123">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de593-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de593-124">-Name</span></span>
<span data-ttu-id="de593-125">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="de593-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de593-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de593-126">-PassThru</span></span>
<span data-ttu-id="de593-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="de593-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de593-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de593-128">-ResourceGroupName</span></span>
<span data-ttu-id="de593-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de593-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de593-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de593-130">-ResourceId</span></span>
<span data-ttu-id="de593-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="de593-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de593-132">-Выпуск</span><span class="sxs-lookup"><span data-stu-id="de593-132">-Rollout</span></span>
<span data-ttu-id="de593-133">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="de593-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de593-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de593-134">-Confirm</span></span>
<span data-ttu-id="de593-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de593-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de593-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de593-136">-WhatIf</span></span>
<span data-ttu-id="de593-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de593-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de593-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de593-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de593-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de593-139">CommonParameters</span></span>
<span data-ttu-id="de593-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de593-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de593-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de593-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de593-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de593-142">INPUTS</span></span>

### <span data-ttu-id="de593-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="de593-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="de593-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de593-144">OUTPUTS</span></span>

### <span data-ttu-id="de593-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de593-145">System.Boolean</span></span>

## <span data-ttu-id="de593-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="de593-146">NOTES</span></span>

## <span data-ttu-id="de593-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de593-147">RELATED LINKS</span></span>

[<span data-ttu-id="de593-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="de593-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="de593-149">Остановить-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="de593-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="de593-150">Restarting-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="de593-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)