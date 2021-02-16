---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240088"
---
# <span data-ttu-id="2d756-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d756-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2d756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d756-102">SYNOPSIS</span></span>
<span data-ttu-id="2d756-103">Развертывание в группе управления</span><span class="sxs-lookup"><span data-stu-id="2d756-103">Get deployment at a management group</span></span>

## <span data-ttu-id="2d756-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d756-104">SYNTAX</span></span>

### <span data-ttu-id="2d756-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d756-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d756-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2d756-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d756-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d756-107">DESCRIPTION</span></span>
<span data-ttu-id="2d756-108">Развертывание в группе управления получает **cmdlet Get-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="2d756-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="2d756-109">Укажите параметр *"Имя"* *или "ИД",* чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="2d756-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="2d756-110">По умолчанию **Get-AzManagementGroupDeployment** получает все развертывания в группе управления.</span><span class="sxs-lookup"><span data-stu-id="2d756-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="2d756-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d756-111">EXAMPLES</span></span>

### <span data-ttu-id="2d756-112">Пример 1. Получить все развертывания в группе управления</span><span class="sxs-lookup"><span data-stu-id="2d756-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="2d756-113">Эта команда получает все развертывания в группе управления MyMG.</span><span class="sxs-lookup"><span data-stu-id="2d756-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="2d756-114">Пример 2. Получить развертывание по имени</span><span class="sxs-lookup"><span data-stu-id="2d756-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="2d756-115">Эта команда получает развертывание Deploy01 в группе управления MyMG.</span><span class="sxs-lookup"><span data-stu-id="2d756-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="2d756-116">Вы можете назначить имя развертыванию при его создании с помощью многлетов **New-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="2d756-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="2d756-117">Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d756-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="2d756-118">Пример 3. Получить развертывание по ИД</span><span class="sxs-lookup"><span data-stu-id="2d756-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="2d756-119">Эта команда получает развертывание Deploy01 в группе управления MyMG.</span><span class="sxs-lookup"><span data-stu-id="2d756-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="2d756-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d756-120">PARAMETERS</span></span>

### <span data-ttu-id="2d756-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d756-121">-DefaultProfile</span></span>
<span data-ttu-id="2d756-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d756-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d756-123">-Id</span><span class="sxs-lookup"><span data-stu-id="2d756-123">-Id</span></span>
<span data-ttu-id="2d756-124">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="2d756-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2d756-125">пример: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2d756-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d756-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2d756-126">-ManagementGroupId</span></span>
<span data-ttu-id="2d756-127">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="2d756-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d756-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2d756-128">-Name</span></span>
<span data-ttu-id="2d756-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d756-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d756-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d756-130">-Pre</span></span>
<span data-ttu-id="2d756-131">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="2d756-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2d756-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d756-132">CommonParameters</span></span>
<span data-ttu-id="2d756-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d756-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d756-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d756-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d756-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d756-135">INPUTS</span></span>

### <span data-ttu-id="2d756-136">Нет</span><span class="sxs-lookup"><span data-stu-id="2d756-136">None</span></span>

## <span data-ttu-id="2d756-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d756-137">OUTPUTS</span></span>

### <span data-ttu-id="2d756-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="2d756-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2d756-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d756-139">NOTES</span></span>

## <span data-ttu-id="2d756-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d756-140">RELATED LINKS</span></span>
