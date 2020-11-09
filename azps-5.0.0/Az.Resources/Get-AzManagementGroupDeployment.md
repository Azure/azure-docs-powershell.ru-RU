---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316464"
---
# <span data-ttu-id="422e4-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="422e4-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="422e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="422e4-102">SYNOPSIS</span></span>
<span data-ttu-id="422e4-103">Получение развертывания в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="422e4-103">Get deployment at a management group</span></span>

## <span data-ttu-id="422e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="422e4-104">SYNTAX</span></span>

### <span data-ttu-id="422e4-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="422e4-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="422e4-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="422e4-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="422e4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="422e4-107">DESCRIPTION</span></span>
<span data-ttu-id="422e4-108">Командлет **Get-AzManagementGroupDeployment** получает развертывание в группе управления.</span><span class="sxs-lookup"><span data-stu-id="422e4-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="422e4-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="422e4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="422e4-110">По умолчанию **Get-AzManagementGroupDeployment** получает все развертывания в группе "Управление".</span><span class="sxs-lookup"><span data-stu-id="422e4-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="422e4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="422e4-111">EXAMPLES</span></span>

### <span data-ttu-id="422e4-112">Пример 1: получение всех развертываний в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="422e4-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="422e4-113">Эта команда получает все развертывания в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="422e4-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="422e4-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="422e4-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="422e4-115">Эта команда получает развертывание "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="422e4-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="422e4-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="422e4-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="422e4-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="422e4-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="422e4-118">Пример 3: получение развертывания по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="422e4-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="422e4-119">Эта команда получает развертывание "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="422e4-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="422e4-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="422e4-120">PARAMETERS</span></span>

### <span data-ttu-id="422e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422e4-121">-DefaultProfile</span></span>
<span data-ttu-id="422e4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="422e4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="422e4-123">-ID</span><span class="sxs-lookup"><span data-stu-id="422e4-123">-Id</span></span>
<span data-ttu-id="422e4-124">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="422e4-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="422e4-125">Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="422e4-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="422e4-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="422e4-126">-ManagementGroupId</span></span>
<span data-ttu-id="422e4-127">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="422e4-127">The management group id.</span></span>

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

### <span data-ttu-id="422e4-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="422e4-128">-Name</span></span>
<span data-ttu-id="422e4-129">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="422e4-129">The name of deployment.</span></span>

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

### <span data-ttu-id="422e4-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="422e4-130">-Pre</span></span>
<span data-ttu-id="422e4-131">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="422e4-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="422e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422e4-132">CommonParameters</span></span>
<span data-ttu-id="422e4-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="422e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422e4-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="422e4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422e4-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="422e4-135">INPUTS</span></span>

### <span data-ttu-id="422e4-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="422e4-136">None</span></span>

## <span data-ttu-id="422e4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="422e4-137">OUTPUTS</span></span>

### <span data-ttu-id="422e4-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="422e4-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="422e4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="422e4-139">NOTES</span></span>

## <span data-ttu-id="422e4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="422e4-140">RELATED LINKS</span></span>
