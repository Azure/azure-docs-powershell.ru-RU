---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316456"
---
# <span data-ttu-id="90e5e-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="90e5e-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="90e5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="90e5e-103">Операция получения развертывания для группы управления</span><span class="sxs-lookup"><span data-stu-id="90e5e-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="90e5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90e5e-104">SYNTAX</span></span>

### <span data-ttu-id="90e5e-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90e5e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90e5e-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="90e5e-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90e5e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="90e5e-108">Командлет **Get-AzManagementGroupDeploymentOperation** перечисляет все операции, которые были частью развертывания группы управления, чтобы помочь вам найти и получить дополнительные сведения о конкретных операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e5e-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="90e5e-109">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="90e5e-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="90e5e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90e5e-110">EXAMPLES</span></span>

### <span data-ttu-id="90e5e-111">Пример 1: получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="90e5e-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="90e5e-112">Возвращает операции развертывания с именем "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="90e5e-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="90e5e-113">Пример 2: получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="90e5e-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="90e5e-114">Эта команда получает развертывание "Deploy01" в группе управления "myMG" и получает операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e5e-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="90e5e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90e5e-115">PARAMETERS</span></span>

### <span data-ttu-id="90e5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e5e-116">-DefaultProfile</span></span>
<span data-ttu-id="90e5e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90e5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e5e-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="90e5e-118">-DeploymentName</span></span>
<span data-ttu-id="90e5e-119">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e5e-119">The deployment name.</span></span>

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

### <span data-ttu-id="90e5e-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="90e5e-120">-DeploymentObject</span></span>
<span data-ttu-id="90e5e-121">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e5e-121">The deployment object.</span></span>

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

### <span data-ttu-id="90e5e-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="90e5e-122">-ManagementGroupId</span></span>
<span data-ttu-id="90e5e-123">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="90e5e-123">The management group id.</span></span>

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

### <span data-ttu-id="90e5e-124">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="90e5e-124">-OperationId</span></span>
<span data-ttu-id="90e5e-125">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e5e-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="90e5e-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="90e5e-126">-Pre</span></span>
<span data-ttu-id="90e5e-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="90e5e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="90e5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e5e-128">CommonParameters</span></span>
<span data-ttu-id="90e5e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90e5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e5e-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90e5e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e5e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90e5e-131">INPUTS</span></span>

### <span data-ttu-id="90e5e-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="90e5e-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="90e5e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90e5e-133">OUTPUTS</span></span>

### <span data-ttu-id="90e5e-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="90e5e-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="90e5e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="90e5e-135">NOTES</span></span>

## <span data-ttu-id="90e5e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90e5e-136">RELATED LINKS</span></span>
