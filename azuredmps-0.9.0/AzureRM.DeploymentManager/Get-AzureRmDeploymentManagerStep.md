---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555415"
---
# <span data-ttu-id="c6e6b-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c6e6b-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="c6e6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e6b-103">Получает шаг развертывания.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-103">Gets the deployment step.</span></span>

## <span data-ttu-id="c6e6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6e6b-104">SYNTAX</span></span>

### <span data-ttu-id="c6e6b-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6e6b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e6b-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6e6b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e6b-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e6b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e6b-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e6b-109">Командлет **Get-AzureRmDeploymentManagerStep** получает шаг и возвращает объект, который представляет этот шаг.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="c6e6b-110">Укажите шаг, указав имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="c6e6b-111">Кроме того, вы можете предоставить объект Step или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="c6e6b-112">Вы можете локально изменить этот объект, а затем применить изменения к источнику артефакта с помощью командлета Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="c6e6b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6e6b-113">EXAMPLES</span></span>

### <span data-ttu-id="c6e6b-114">Пример 1: получение шага</span><span class="sxs-lookup"><span data-stu-id="c6e6b-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="c6e6b-115">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c6e6b-116">Пример 2: получение шага с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="c6e6b-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="c6e6b-117">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c6e6b-118">Пример 3: получение шага с помощью объекта, возвращаемого New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c6e6b-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="c6e6b-119">Эта команда получает шаг, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="c6e6b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6e6b-120">PARAMETERS</span></span>

### <span data-ttu-id="c6e6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e6b-121">-DefaultProfile</span></span>
<span data-ttu-id="c6e6b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e6b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-123">-Name</span></span>
<span data-ttu-id="c6e6b-124">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-124">The name of the step.</span></span>

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

### <span data-ttu-id="c6e6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6e6b-126">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-126">The resource group.</span></span>

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

### <span data-ttu-id="c6e6b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e6b-127">-ResourceId</span></span>
<span data-ttu-id="c6e6b-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-128">The resource identifier.</span></span>

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

### <span data-ttu-id="c6e6b-129">-Шаг</span><span class="sxs-lookup"><span data-stu-id="c6e6b-129">-Step</span></span>
<span data-ttu-id="c6e6b-130">Объект шага "ресурс".</span><span class="sxs-lookup"><span data-stu-id="c6e6b-130">The step resource object.</span></span>

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

### <span data-ttu-id="c6e6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e6b-131">CommonParameters</span></span>
<span data-ttu-id="c6e6b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c6e6b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e6b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e6b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6e6b-134">INPUTS</span></span>

### <span data-ttu-id="c6e6b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e6b-135">System.String</span></span>

### <span data-ttu-id="c6e6b-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c6e6b-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c6e6b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e6b-137">OUTPUTS</span></span>

### <span data-ttu-id="c6e6b-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c6e6b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c6e6b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6e6b-139">NOTES</span></span>

## <span data-ttu-id="c6e6b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6e6b-140">RELATED LINKS</span></span>
