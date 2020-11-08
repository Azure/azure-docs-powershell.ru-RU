---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074395"
---
# <span data-ttu-id="ade37-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ade37-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ade37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ade37-102">SYNOPSIS</span></span>
<span data-ttu-id="ade37-103">Получает выпуск.</span><span class="sxs-lookup"><span data-stu-id="ade37-103">Gets the rollout.</span></span>

## <span data-ttu-id="ade37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ade37-104">SYNTAX</span></span>

### <span data-ttu-id="ade37-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade37-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade37-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ade37-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ade37-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ade37-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ade37-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade37-108">DESCRIPTION</span></span>
<span data-ttu-id="ade37-109">Командлет **Get-AzDeploymentManagerRollout** получает сообщение о выпуске и возвращает объект, который представляет этот выпуск с подробными сведениями о ходе выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ade37-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade37-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ade37-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="ade37-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="ade37-112">Возвращенный объект содержит службы, единицы обслуживания и шаги, которые были развернуты, и выполняющиеся задачи.</span><span class="sxs-lookup"><span data-stu-id="ade37-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="ade37-113">Те, которые еще не развернуты, не в ответе.</span><span class="sxs-lookup"><span data-stu-id="ade37-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="ade37-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ade37-114">EXAMPLES</span></span>

### <span data-ttu-id="ade37-115">Пример 1 получение выпуска</span><span class="sxs-lookup"><span data-stu-id="ade37-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ade37-116">Эта команда возвращает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ade37-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="ade37-117">Пример 2. получение и отображение сведений о выпуске</span><span class="sxs-lookup"><span data-stu-id="ade37-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="ade37-118">Эта команда возвращает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ade37-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="ade37-119">Параметр-подробное отображение всех сведений о выпуске в иерархии; показаны службы, ServiceUnits и шаги, описанные в разделе каждый ServiceUnit и контекстные сведения для каждого шага для комплексного представления выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="ade37-120">Пример 3: получение выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="ade37-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ade37-121">Эта команда возвращает выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ade37-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ade37-122">Пример 4: получение выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ade37-123">Эта команда возвращает выгрузку, имя и значение ResourceGroup которой совпадают со свойствами Name и ResourceGroupName для $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="ade37-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ade37-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ade37-124">PARAMETERS</span></span>

### <span data-ttu-id="ade37-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade37-125">-DefaultProfile</span></span>
<span data-ttu-id="ade37-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ade37-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade37-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade37-127">-InputObject</span></span>
<span data-ttu-id="ade37-128">Объект выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-128">Rollout object.</span></span>

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

### <span data-ttu-id="ade37-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ade37-129">-Name</span></span>
<span data-ttu-id="ade37-130">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-130">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade37-131">-ResourceGroupName</span></span>
<span data-ttu-id="ade37-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade37-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade37-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ade37-133">-ResourceId</span></span>
<span data-ttu-id="ade37-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ade37-134">The resource identifier.</span></span>

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

### <span data-ttu-id="ade37-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="ade37-135">-RetryAttempt</span></span>
<span data-ttu-id="ade37-136">Повторная попытка выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade37-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade37-137">CommonParameters</span></span>
<span data-ttu-id="ade37-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ade37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade37-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ade37-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade37-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ade37-140">INPUTS</span></span>

### <span data-ttu-id="ade37-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ade37-141">System.String</span></span>

### <span data-ttu-id="ade37-142">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ade37-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ade37-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ade37-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ade37-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade37-144">OUTPUTS</span></span>

### <span data-ttu-id="ade37-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ade37-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ade37-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ade37-146">NOTES</span></span>

## <span data-ttu-id="ade37-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade37-147">RELATED LINKS</span></span>
