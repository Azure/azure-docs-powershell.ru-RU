---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079352"
---
# <span data-ttu-id="fb7b2-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="fb7b2-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="fb7b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7b2-103">Получить развертывание в области клиента</span><span class="sxs-lookup"><span data-stu-id="fb7b2-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="fb7b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb7b2-104">SYNTAX</span></span>

### <span data-ttu-id="fb7b2-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb7b2-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7b2-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="fb7b2-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7b2-108">Командлет **Get-AzTenantDeployment** получает развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="fb7b2-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="fb7b2-110">По умолчанию **Get-AzTenantDeployment** получает все развертывания в области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="fb7b2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb7b2-111">EXAMPLES</span></span>

### <span data-ttu-id="fb7b2-112">Пример 1: получение всех развертываний в области клиента</span><span class="sxs-lookup"><span data-stu-id="fb7b2-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="fb7b2-113">Эта команда получает все развертывания в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="fb7b2-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="fb7b2-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="fb7b2-115">Эта команда получает развертывание "Deploy01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="fb7b2-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="fb7b2-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="fb7b2-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="fb7b2-118">Пример 3: получение развертывания по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fb7b2-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="fb7b2-119">Эта команда получает развертывание "Deploy01" в области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="fb7b2-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb7b2-120">PARAMETERS</span></span>

### <span data-ttu-id="fb7b2-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb7b2-121">-ApiVersion</span></span>
<span data-ttu-id="fb7b2-122">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb7b2-123">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fb7b2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7b2-124">-DefaultProfile</span></span>
<span data-ttu-id="fb7b2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7b2-126">-ID</span><span class="sxs-lookup"><span data-stu-id="fb7b2-126">-Id</span></span>
<span data-ttu-id="fb7b2-127">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="fb7b2-128">Пример:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="fb7b2-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="fb7b2-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb7b2-129">-Name</span></span>
<span data-ttu-id="fb7b2-130">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7b2-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb7b2-131">-Pre</span></span>
<span data-ttu-id="fb7b2-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb7b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7b2-133">CommonParameters</span></span>
<span data-ttu-id="fb7b2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7b2-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb7b2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7b2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb7b2-136">INPUTS</span></span>

### <span data-ttu-id="fb7b2-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="fb7b2-137">None</span></span>

## <span data-ttu-id="fb7b2-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb7b2-138">OUTPUTS</span></span>

### <span data-ttu-id="fb7b2-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fb7b2-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fb7b2-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb7b2-140">NOTES</span></span>

## <span data-ttu-id="fb7b2-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb7b2-141">RELATED LINKS</span></span>
