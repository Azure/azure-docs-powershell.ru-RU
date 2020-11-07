---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913553"
---
# <span data-ttu-id="733cf-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="733cf-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="733cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="733cf-102">SYNOPSIS</span></span>
<span data-ttu-id="733cf-103">Получить развертывание</span><span class="sxs-lookup"><span data-stu-id="733cf-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="733cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="733cf-104">SYNTAX</span></span>

### <span data-ttu-id="733cf-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="733cf-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="733cf-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="733cf-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="733cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="733cf-107">DESCRIPTION</span></span>
<span data-ttu-id="733cf-108">Командлет **Get-AzureRmDeployment** получает развертывание в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="733cf-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="733cf-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="733cf-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="733cf-110">По умолчанию **Get-AzureRmDeployment** получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="733cf-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="733cf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="733cf-111">EXAMPLES</span></span>

### <span data-ttu-id="733cf-112">Пример 1: получение всех развертываний в области подписки</span><span class="sxs-lookup"><span data-stu-id="733cf-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="733cf-113">Эта команда получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="733cf-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="733cf-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="733cf-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="733cf-115">Эта команда получает развертывание DeployRoles01 в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="733cf-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="733cf-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="733cf-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="733cf-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="733cf-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="733cf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="733cf-118">PARAMETERS</span></span>

### <span data-ttu-id="733cf-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="733cf-119">-ApiVersion</span></span>
<span data-ttu-id="733cf-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="733cf-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="733cf-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="733cf-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="733cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733cf-122">-DefaultProfile</span></span>
<span data-ttu-id="733cf-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="733cf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="733cf-124">-ID</span><span class="sxs-lookup"><span data-stu-id="733cf-124">-Id</span></span>
<span data-ttu-id="733cf-125">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="733cf-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="733cf-126">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="733cf-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="733cf-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="733cf-127">-Name</span></span>
<span data-ttu-id="733cf-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="733cf-128">The name of deployment.</span></span>

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

### <span data-ttu-id="733cf-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="733cf-129">-Pre</span></span>
<span data-ttu-id="733cf-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="733cf-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="733cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733cf-131">CommonParameters</span></span>
<span data-ttu-id="733cf-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="733cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733cf-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733cf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733cf-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="733cf-134">INPUTS</span></span>

### <span data-ttu-id="733cf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="733cf-135">System.String</span></span>

## <span data-ttu-id="733cf-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="733cf-136">OUTPUTS</span></span>

### <span data-ttu-id="733cf-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="733cf-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="733cf-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="733cf-138">NOTES</span></span>

## <span data-ttu-id="733cf-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="733cf-139">RELATED LINKS</span></span>
