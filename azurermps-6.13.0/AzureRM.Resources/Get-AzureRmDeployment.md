---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
ms.openlocfilehash: 6d25bcf98adb740ec695152eb5b27ec9402082c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732584"
---
# <span data-ttu-id="f3ec2-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f3ec2-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="f3ec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ec2-103">Получить развертывание</span><span class="sxs-lookup"><span data-stu-id="f3ec2-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3ec2-104">SYNTAX</span></span>

### <span data-ttu-id="f3ec2-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3ec2-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ec2-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f3ec2-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ec2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ec2-108">Командлет **Get-AzureRmDeployment** получает развертывание в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="f3ec2-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="f3ec2-110">По умолчанию **Get-AzureRmDeployment** получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="f3ec2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3ec2-111">EXAMPLES</span></span>

### <span data-ttu-id="f3ec2-112">Пример 1: получение всех развертываний в области подписки</span><span class="sxs-lookup"><span data-stu-id="f3ec2-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="f3ec2-113">Эта команда получает все развертывания в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="f3ec2-114">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="f3ec2-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="f3ec2-115">Эта команда получает развертывание DeployRoles01 в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="f3ec2-116">Вы можете присвоить имя развертыванию при его создании с помощью командлетов **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f3ec2-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="f3ec2-117">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="f3ec2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3ec2-118">PARAMETERS</span></span>

### <span data-ttu-id="f3ec2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3ec2-119">-ApiVersion</span></span>
<span data-ttu-id="f3ec2-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f3ec2-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f3ec2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ec2-122">-DefaultProfile</span></span>
<span data-ttu-id="f3ec2-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ec2-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f3ec2-124">-Id</span></span>
<span data-ttu-id="f3ec2-125">Полный идентификатор ресурса для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f3ec2-126">Пример:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f3ec2-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="f3ec2-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3ec2-127">-Name</span></span>
<span data-ttu-id="f3ec2-128">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-128">The name of deployment.</span></span>

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

### <span data-ttu-id="f3ec2-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3ec2-129">-Pre</span></span>
<span data-ttu-id="f3ec2-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f3ec2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ec2-131">CommonParameters</span></span>
<span data-ttu-id="f3ec2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3ec2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ec2-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ec2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ec2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3ec2-134">INPUTS</span></span>

### <span data-ttu-id="f3ec2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f3ec2-135">System.String</span></span>

## <span data-ttu-id="f3ec2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ec2-136">OUTPUTS</span></span>

### <span data-ttu-id="f3ec2-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f3ec2-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f3ec2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3ec2-138">NOTES</span></span>

## <span data-ttu-id="f3ec2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3ec2-139">RELATED LINKS</span></span>
