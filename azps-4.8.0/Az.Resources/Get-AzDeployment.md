---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 5ea6e36adeb1c0b220b87d516e9c236907bc2c63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235455"
---
# <span data-ttu-id="10798-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="10798-101">Get-AzDeployment</span></span>

## <span data-ttu-id="10798-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10798-102">SYNOPSIS</span></span>
<span data-ttu-id="10798-103">Получить развертывание</span><span class="sxs-lookup"><span data-stu-id="10798-103">Get deployment</span></span>

## <span data-ttu-id="10798-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10798-104">SYNTAX</span></span>

### <span data-ttu-id="10798-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10798-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10798-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="10798-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10798-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10798-107">DESCRIPTION</span></span>
<span data-ttu-id="10798-108">Командлет **Get-AzDeployment** получает развертывание в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="10798-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="10798-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="10798-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="10798-110">По умолчанию **Get-AzDeployment** получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="10798-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="10798-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10798-111">EXAMPLES</span></span>

### <span data-ttu-id="10798-112">Пример 1: получение всех развертываний в области подписки</span><span class="sxs-lookup"><span data-stu-id="10798-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="10798-113">Эта команда получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="10798-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="10798-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="10798-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="10798-115">Эта команда получает развертывание DeployRoles01 в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="10798-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="10798-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="10798-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="10798-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="10798-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="10798-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10798-118">PARAMETERS</span></span>

### <span data-ttu-id="10798-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="10798-119">-ApiVersion</span></span>
<span data-ttu-id="10798-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10798-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="10798-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="10798-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="10798-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10798-122">-DefaultProfile</span></span>
<span data-ttu-id="10798-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10798-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10798-124">-ID</span><span class="sxs-lookup"><span data-stu-id="10798-124">-Id</span></span>
<span data-ttu-id="10798-125">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="10798-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="10798-126">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="10798-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="10798-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10798-127">-Name</span></span>
<span data-ttu-id="10798-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="10798-128">The name of deployment.</span></span>

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

### <span data-ttu-id="10798-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="10798-129">-Pre</span></span>
<span data-ttu-id="10798-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="10798-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="10798-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10798-131">CommonParameters</span></span>
<span data-ttu-id="10798-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10798-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10798-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10798-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10798-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10798-134">INPUTS</span></span>

### <span data-ttu-id="10798-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="10798-135">None</span></span>

## <span data-ttu-id="10798-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10798-136">OUTPUTS</span></span>

### <span data-ttu-id="10798-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="10798-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="10798-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="10798-138">NOTES</span></span>

## <span data-ttu-id="10798-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10798-139">RELATED LINKS</span></span>
