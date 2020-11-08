---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244227"
---
# <span data-ttu-id="a74d6-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a74d6-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="a74d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a74d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a74d6-103">Получение развертывания в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="a74d6-103">Get deployment at a management group</span></span>

## <span data-ttu-id="a74d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a74d6-104">SYNTAX</span></span>

### <span data-ttu-id="a74d6-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a74d6-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a74d6-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a74d6-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a74d6-107">DESCRIPTION</span></span>
<span data-ttu-id="a74d6-108">Командлет **Get-AzManagementGroupDeployment** получает развертывание в группе управления.</span><span class="sxs-lookup"><span data-stu-id="a74d6-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="a74d6-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="a74d6-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a74d6-110">По умолчанию **Get-AzManagementGroupDeployment** получает все развертывания в группе "Управление".</span><span class="sxs-lookup"><span data-stu-id="a74d6-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="a74d6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a74d6-111">EXAMPLES</span></span>

### <span data-ttu-id="a74d6-112">Пример 1: получение всех развертываний в группе "Управление"</span><span class="sxs-lookup"><span data-stu-id="a74d6-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="a74d6-113">Эта команда получает все развертывания в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="a74d6-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="a74d6-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="a74d6-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="a74d6-115">Эта команда получает развертывание "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="a74d6-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="a74d6-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="a74d6-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="a74d6-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="a74d6-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="a74d6-118">Пример 3: получение развертывания по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="a74d6-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="a74d6-119">Эта команда получает развертывание "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="a74d6-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="a74d6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a74d6-120">PARAMETERS</span></span>

### <span data-ttu-id="a74d6-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a74d6-121">-ApiVersion</span></span>
<span data-ttu-id="a74d6-122">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a74d6-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a74d6-123">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="a74d6-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74d6-124">-DefaultProfile</span></span>
<span data-ttu-id="a74d6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a74d6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a74d6-126">-Id</span></span>
<span data-ttu-id="a74d6-127">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="a74d6-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a74d6-128">Пример:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a74d6-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a74d6-129">-ManagementGroupId</span></span>
<span data-ttu-id="a74d6-130">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="a74d6-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a74d6-131">-Name</span></span>
<span data-ttu-id="a74d6-132">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="a74d6-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="a74d6-133">-Pre</span></span>
<span data-ttu-id="a74d6-134">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="a74d6-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74d6-135">CommonParameters</span></span>
<span data-ttu-id="a74d6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a74d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74d6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a74d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74d6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a74d6-138">INPUTS</span></span>

### <span data-ttu-id="a74d6-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="a74d6-139">None</span></span>

## <span data-ttu-id="a74d6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a74d6-140">OUTPUTS</span></span>

### <span data-ttu-id="a74d6-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a74d6-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a74d6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a74d6-142">NOTES</span></span>

## <span data-ttu-id="a74d6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a74d6-143">RELATED LINKS</span></span>
