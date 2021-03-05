---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960120"
---
# <span data-ttu-id="f2ba8-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f2ba8-101">Get-AzDeployment</span></span>

## <span data-ttu-id="f2ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ba8-103">Получить развертывание</span><span class="sxs-lookup"><span data-stu-id="f2ba8-103">Get deployment</span></span>

## <span data-ttu-id="f2ba8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2ba8-104">SYNTAX</span></span>

### <span data-ttu-id="f2ba8-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2ba8-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ba8-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f2ba8-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ba8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2ba8-107">DESCRIPTION</span></span>
<span data-ttu-id="f2ba8-108">Для развертывания требуется текущая область действия подписки с использованием **cmdlet Get-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="f2ba8-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="f2ba8-109">Укажите *параметр "Имя"* *или "ИД",* чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="f2ba8-110">По умолчанию **Get-AzDeployment** получает все развертывания с текущей областью действия подписки.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="f2ba8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2ba8-111">EXAMPLES</span></span>

### <span data-ttu-id="f2ba8-112">Пример 1. Все развертывания в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="f2ba8-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="f2ba8-113">Эта команда получает все развертывания в текущей области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="f2ba8-114">Пример 2. Получить развертывание по имени</span><span class="sxs-lookup"><span data-stu-id="f2ba8-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="f2ba8-115">Эта команда получает развертывание DeployRoles01 в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="f2ba8-116">Вы можете назначить имя развертыванию при его создании с помощью проектлетов **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="f2ba8-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="f2ba8-117">Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="f2ba8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-118">PARAMETERS</span></span>

### <span data-ttu-id="f2ba8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ba8-119">-DefaultProfile</span></span>
<span data-ttu-id="f2ba8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ba8-121">-Id</span><span class="sxs-lookup"><span data-stu-id="f2ba8-121">-Id</span></span>
<span data-ttu-id="f2ba8-122">Полное ид ресурса в развертывании.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f2ba8-123">пример: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f2ba8-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="f2ba8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f2ba8-124">-Name</span></span>
<span data-ttu-id="f2ba8-125">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-125">The name of deployment.</span></span>

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

### <span data-ttu-id="f2ba8-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2ba8-126">-Pre</span></span>
<span data-ttu-id="f2ba8-127">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f2ba8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ba8-128">CommonParameters</span></span>
<span data-ttu-id="f2ba8-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ba8-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2ba8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ba8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-131">INPUTS</span></span>

### <span data-ttu-id="f2ba8-132">Нет</span><span class="sxs-lookup"><span data-stu-id="f2ba8-132">None</span></span>

## <span data-ttu-id="f2ba8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-133">OUTPUTS</span></span>

### <span data-ttu-id="f2ba8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="f2ba8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f2ba8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2ba8-135">NOTES</span></span>

## <span data-ttu-id="f2ba8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2ba8-136">RELATED LINKS</span></span>
