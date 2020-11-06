---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555396"
---
# <span data-ttu-id="b9931-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b9931-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="b9931-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9931-102">SYNOPSIS</span></span>
<span data-ttu-id="b9931-103">Удаление шага.</span><span class="sxs-lookup"><span data-stu-id="b9931-103">Deletes a step.</span></span>

## <span data-ttu-id="b9931-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9931-104">SYNTAX</span></span>

### <span data-ttu-id="b9931-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9931-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9931-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9931-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9931-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9931-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9931-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9931-108">DESCRIPTION</span></span>
<span data-ttu-id="b9931-109">Командлет **Remove-AzureRmDeploymentManagerStep** удаляет шаг.</span><span class="sxs-lookup"><span data-stu-id="b9931-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="b9931-110">Укажите шаг, указав имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9931-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="b9931-111">Кроме того, вы можете предоставить объект Step или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b9931-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="b9931-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9931-112">EXAMPLES</span></span>
### <span data-ttu-id="b9931-113">Пример 1: удаление шага</span><span class="sxs-lookup"><span data-stu-id="b9931-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b9931-114">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9931-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b9931-115">Пример 2: удаление шага с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="b9931-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b9931-116">Эта команда удаляет шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9931-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b9931-117">Пример 3: удаление шага с помощью объекта, возвращаемого New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b9931-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="b9931-118">Эта команда удаляет шаг, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b9931-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="b9931-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9931-119">PARAMETERS</span></span>

### <span data-ttu-id="b9931-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9931-120">-DefaultProfile</span></span>
<span data-ttu-id="b9931-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9931-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9931-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b9931-122">-Force</span></span>
<span data-ttu-id="b9931-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b9931-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9931-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9931-124">-Name</span></span>
<span data-ttu-id="b9931-125">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="b9931-125">The name of the step.</span></span>

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

### <span data-ttu-id="b9931-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9931-126">-PassThru</span></span>
<span data-ttu-id="b9931-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="b9931-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b9931-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9931-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9931-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9931-129">The resource group.</span></span>

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

### <span data-ttu-id="b9931-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9931-130">-ResourceId</span></span>
<span data-ttu-id="b9931-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9931-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b9931-132">-Шаг</span><span class="sxs-lookup"><span data-stu-id="b9931-132">-Step</span></span>
<span data-ttu-id="b9931-133">Шаг, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b9931-133">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9931-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9931-134">-Confirm</span></span>
<span data-ttu-id="b9931-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9931-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9931-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9931-136">-WhatIf</span></span>
<span data-ttu-id="b9931-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9931-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9931-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9931-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9931-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9931-139">CommonParameters</span></span>
<span data-ttu-id="b9931-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9931-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b9931-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9931-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9931-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9931-142">INPUTS</span></span>

### <span data-ttu-id="b9931-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b9931-143">System.String</span></span>

### <span data-ttu-id="b9931-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b9931-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b9931-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9931-145">OUTPUTS</span></span>

### <span data-ttu-id="b9931-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9931-146">System.Boolean</span></span>

## <span data-ttu-id="b9931-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9931-147">NOTES</span></span>

## <span data-ttu-id="b9931-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9931-148">RELATED LINKS</span></span>
