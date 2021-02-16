---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226833"
---
# <span data-ttu-id="6e1ba-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6e1ba-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="6e1ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1ba-103">Развертывание в области клиента</span><span class="sxs-lookup"><span data-stu-id="6e1ba-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="6e1ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e1ba-104">SYNTAX</span></span>

### <span data-ttu-id="6e1ba-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e1ba-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e1ba-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6e1ba-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1ba-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e1ba-107">DESCRIPTION</span></span>
<span data-ttu-id="6e1ba-108">Для развертывания в области клиента развертывание возвращается с использованием **cmdlet Get-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="6e1ba-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="6e1ba-109">Укажите параметр *"Имя"* *или "ИД",* чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="6e1ba-110">По умолчанию **Get-AzTenantDeployment** получает все развертывания в области клиента.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="6e1ba-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e1ba-111">EXAMPLES</span></span>

### <span data-ttu-id="6e1ba-112">Пример 1. Получить все развертывания в рамках клиента</span><span class="sxs-lookup"><span data-stu-id="6e1ba-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="6e1ba-113">Эта команда получает все развертывания в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="6e1ba-114">Пример 2. Получить развертывание по имени</span><span class="sxs-lookup"><span data-stu-id="6e1ba-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="6e1ba-115">Эта команда получает развертывание Deploy01 в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="6e1ba-116">Вы можете назначить имя развертыванию при его создании с помощью выполнения с помощью проектлетов **New-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="6e1ba-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="6e1ba-117">Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="6e1ba-118">Пример 3. Получить развертывание по ИД</span><span class="sxs-lookup"><span data-stu-id="6e1ba-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="6e1ba-119">Эта команда получает развертывание Deploy01 в области клиента.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="6e1ba-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1ba-120">PARAMETERS</span></span>

### <span data-ttu-id="6e1ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1ba-121">-DefaultProfile</span></span>
<span data-ttu-id="6e1ba-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1ba-123">-Id</span><span class="sxs-lookup"><span data-stu-id="6e1ba-123">-Id</span></span>
<span data-ttu-id="6e1ba-124">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6e1ba-125">пример: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6e1ba-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="6e1ba-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6e1ba-126">-Name</span></span>
<span data-ttu-id="6e1ba-127">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1ba-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e1ba-128">-Pre</span></span>
<span data-ttu-id="6e1ba-129">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e1ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1ba-130">CommonParameters</span></span>
<span data-ttu-id="6e1ba-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1ba-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1ba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1ba-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1ba-133">INPUTS</span></span>

### <span data-ttu-id="6e1ba-134">Нет</span><span class="sxs-lookup"><span data-stu-id="6e1ba-134">None</span></span>

## <span data-ttu-id="6e1ba-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1ba-135">OUTPUTS</span></span>

### <span data-ttu-id="6e1ba-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="6e1ba-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6e1ba-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e1ba-137">NOTES</span></span>

## <span data-ttu-id="6e1ba-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e1ba-138">RELATED LINKS</span></span>
