---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555160"
---
# <span data-ttu-id="590b1-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="590b1-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="590b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="590b1-102">SYNOPSIS</span></span>
<span data-ttu-id="590b1-103">Получение выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-103">Gets a rollout.</span></span>

## <span data-ttu-id="590b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="590b1-104">SYNTAX</span></span>

### <span data-ttu-id="590b1-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="590b1-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590b1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="590b1-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="590b1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="590b1-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="590b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="590b1-108">DESCRIPTION</span></span>
<span data-ttu-id="590b1-109">Командлет **Get-AzureRmDeploymentManagerRollout** получает сообщение о выпуске и возвращает объект, который представляет этот выпуск с подробными сведениями о ходе выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="590b1-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="590b1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="590b1-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="590b1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="590b1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="590b1-112">EXAMPLES</span></span>

### <span data-ttu-id="590b1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="590b1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="590b1-114">Эта команда возвращает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="590b1-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="590b1-115">Пример 2: получение выпусков с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="590b1-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="590b1-116">Эта команда возвращает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="590b1-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="590b1-117">Пример 3: получение выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="590b1-118">Эта команда возвращает выгрузку, имя и значение ResourceGroup которой совпадают со свойствами Name и ResourceGroupName для $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="590b1-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="590b1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="590b1-119">PARAMETERS</span></span>

### <span data-ttu-id="590b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590b1-120">-DefaultProfile</span></span>
<span data-ttu-id="590b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="590b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="590b1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="590b1-122">-Name</span></span>
<span data-ttu-id="590b1-123">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="590b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="590b1-125">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="590b1-125">The resource group.</span></span>

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

### <span data-ttu-id="590b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="590b1-126">-ResourceId</span></span>
<span data-ttu-id="590b1-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="590b1-127">The resource identifier.</span></span>

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

### <span data-ttu-id="590b1-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="590b1-128">-RetryAttempt</span></span>
<span data-ttu-id="590b1-129">Повторная попытка выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="590b1-130">-Выпуск</span><span class="sxs-lookup"><span data-stu-id="590b1-130">-Rollout</span></span>
<span data-ttu-id="590b1-131">Объект выпуска.</span><span class="sxs-lookup"><span data-stu-id="590b1-131">Rollout object.</span></span>

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

### <span data-ttu-id="590b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590b1-132">CommonParameters</span></span>
<span data-ttu-id="590b1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="590b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590b1-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="590b1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590b1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="590b1-135">INPUTS</span></span>

### <span data-ttu-id="590b1-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="590b1-136">None</span></span>

## <span data-ttu-id="590b1-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="590b1-137">OUTPUTS</span></span>

### <span data-ttu-id="590b1-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="590b1-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="590b1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="590b1-139">NOTES</span></span>

## <span data-ttu-id="590b1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="590b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="590b1-141">Остановить-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="590b1-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="590b1-142">Restarting-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="590b1-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="590b1-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="590b1-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)