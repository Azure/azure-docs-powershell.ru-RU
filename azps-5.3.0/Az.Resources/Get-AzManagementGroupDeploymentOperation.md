---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505287"
---
# <span data-ttu-id="a8733-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a8733-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="a8733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8733-102">SYNOPSIS</span></span>
<span data-ttu-id="a8733-103">Получить операцию развертывания для развертывания группы управления</span><span class="sxs-lookup"><span data-stu-id="a8733-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="a8733-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8733-104">SYNTAX</span></span>

### <span data-ttu-id="a8733-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8733-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8733-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a8733-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8733-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8733-107">DESCRIPTION</span></span>
<span data-ttu-id="a8733-108">С помощью команды **Get-AzManagementGroupDeploymentOperation** перечислены все операции, которые были частью развертывания группы управления, чтобы помочь вам определить и предоставить более подробную информацию об операциях, которые не удалось установить для конкретного развертывания.</span><span class="sxs-lookup"><span data-stu-id="a8733-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a8733-109">Эти же сведения можно получить в сведениях о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="a8733-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="a8733-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8733-110">EXAMPLES</span></span>

### <span data-ttu-id="a8733-111">Пример 1. Получить операции развертывания с именем развертывания</span><span class="sxs-lookup"><span data-stu-id="a8733-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="a8733-112">Получает операции развертывания с именем Deploy01 в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="a8733-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="a8733-113">Пример 2. Получить развертывание и получить операции его развертывания</span><span class="sxs-lookup"><span data-stu-id="a8733-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="a8733-114">Эта команда получает "Deploy01" в группе управления MyMG и получает операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="a8733-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="a8733-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8733-115">PARAMETERS</span></span>

### <span data-ttu-id="a8733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8733-116">-DefaultProfile</span></span>
<span data-ttu-id="a8733-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8733-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8733-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a8733-118">-DeploymentName</span></span>
<span data-ttu-id="a8733-119">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="a8733-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8733-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a8733-120">-DeploymentObject</span></span>
<span data-ttu-id="a8733-121">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="a8733-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8733-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a8733-122">-ManagementGroupId</span></span>
<span data-ttu-id="a8733-123">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="a8733-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8733-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a8733-124">-OperationId</span></span>
<span data-ttu-id="a8733-125">ИД операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="a8733-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8733-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="a8733-126">-Pre</span></span>
<span data-ttu-id="a8733-127">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="a8733-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a8733-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8733-128">CommonParameters</span></span>
<span data-ttu-id="a8733-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8733-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8733-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8733-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8733-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8733-131">INPUTS</span></span>

### <span data-ttu-id="a8733-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="a8733-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a8733-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8733-133">OUTPUTS</span></span>

### <span data-ttu-id="a8733-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a8733-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="a8733-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8733-135">NOTES</span></span>

## <span data-ttu-id="a8733-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8733-136">RELATED LINKS</span></span>
