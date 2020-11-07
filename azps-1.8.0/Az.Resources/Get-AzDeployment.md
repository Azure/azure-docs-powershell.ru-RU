---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729447"
---
# <span data-ttu-id="6f5b4-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f5b4-101">Get-AzDeployment</span></span>

## <span data-ttu-id="6f5b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5b4-103">Получить развертывание</span><span class="sxs-lookup"><span data-stu-id="6f5b4-103">Get deployment</span></span>

## <span data-ttu-id="6f5b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f5b4-104">SYNTAX</span></span>

### <span data-ttu-id="6f5b4-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f5b4-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f5b4-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6f5b4-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f5b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f5b4-107">DESCRIPTION</span></span>
<span data-ttu-id="6f5b4-108">Командлет **Get-AzDeployment** получает развертывание в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="6f5b4-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="6f5b4-110">По умолчанию **Get-AzDeployment** получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="6f5b4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f5b4-111">EXAMPLES</span></span>

### <span data-ttu-id="6f5b4-112">Пример 1: получение всех развертываний в области подписки</span><span class="sxs-lookup"><span data-stu-id="6f5b4-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="6f5b4-113">Эта команда получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="6f5b4-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="6f5b4-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="6f5b4-115">Эта команда получает развертывание DeployRoles01 в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="6f5b4-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="6f5b4-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="6f5b4-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="6f5b4-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f5b4-118">PARAMETERS</span></span>

### <span data-ttu-id="6f5b4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f5b4-119">-ApiVersion</span></span>
<span data-ttu-id="6f5b4-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f5b4-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-121">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5b4-122">-DefaultProfile</span></span>
<span data-ttu-id="6f5b4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5b4-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6f5b4-124">-Id</span></span>
<span data-ttu-id="6f5b4-125">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6f5b4-126">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6f5b4-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5b4-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f5b4-127">-Name</span></span>
<span data-ttu-id="6f5b4-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-128">The name of deployment.</span></span>

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

### <span data-ttu-id="6f5b4-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f5b4-129">-Pre</span></span>
<span data-ttu-id="6f5b4-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6f5b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5b4-131">CommonParameters</span></span>
<span data-ttu-id="6f5b4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5b4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5b4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5b4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f5b4-134">INPUTS</span></span>

### <span data-ttu-id="6f5b4-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f5b4-135">None</span></span>

## <span data-ttu-id="6f5b4-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f5b4-136">OUTPUTS</span></span>

### <span data-ttu-id="6f5b4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6f5b4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6f5b4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f5b4-138">NOTES</span></span>

## <span data-ttu-id="6f5b4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f5b4-139">RELATED LINKS</span></span>
