---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912617"
---
# <span data-ttu-id="689ba-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="689ba-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="689ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="689ba-102">SYNOPSIS</span></span>
<span data-ttu-id="689ba-103">Операция получения развертывания для группы управления</span><span class="sxs-lookup"><span data-stu-id="689ba-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="689ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="689ba-104">SYNTAX</span></span>

### <span data-ttu-id="689ba-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="689ba-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="689ba-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="689ba-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="689ba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="689ba-107">DESCRIPTION</span></span>
<span data-ttu-id="689ba-108">Командлет **Get-AzManagementGroupDeploymentOperation** перечисляет все операции, которые были частью развертывания группы управления, чтобы помочь вам найти и получить дополнительные сведения о конкретных операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="689ba-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="689ba-109">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="689ba-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="689ba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="689ba-110">EXAMPLES</span></span>

### <span data-ttu-id="689ba-111">Пример 1: получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="689ba-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="689ba-112">Возвращает операции развертывания с именем "Deploy01" в группе управления "myMG".</span><span class="sxs-lookup"><span data-stu-id="689ba-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="689ba-113">Пример 2: получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="689ba-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="689ba-114">Эта команда получает развертывание "Deploy01" в группе управления "myMG" и получает операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="689ba-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="689ba-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="689ba-115">PARAMETERS</span></span>

### <span data-ttu-id="689ba-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="689ba-116">-ApiVersion</span></span>
<span data-ttu-id="689ba-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="689ba-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="689ba-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="689ba-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="689ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689ba-119">-DefaultProfile</span></span>
<span data-ttu-id="689ba-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="689ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689ba-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="689ba-121">-DeploymentName</span></span>
<span data-ttu-id="689ba-122">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="689ba-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689ba-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="689ba-123">-DeploymentObject</span></span>
<span data-ttu-id="689ba-124">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="689ba-124">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="689ba-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="689ba-125">-ManagementGroupId</span></span>
<span data-ttu-id="689ba-126">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="689ba-126">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689ba-127">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="689ba-127">-OperationId</span></span>
<span data-ttu-id="689ba-128">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="689ba-128">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689ba-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="689ba-129">-Pre</span></span>
<span data-ttu-id="689ba-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="689ba-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="689ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689ba-131">CommonParameters</span></span>
<span data-ttu-id="689ba-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="689ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689ba-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="689ba-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689ba-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="689ba-134">INPUTS</span></span>

### <span data-ttu-id="689ba-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="689ba-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="689ba-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="689ba-136">OUTPUTS</span></span>

### <span data-ttu-id="689ba-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="689ba-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="689ba-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="689ba-138">NOTES</span></span>

## <span data-ttu-id="689ba-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="689ba-139">RELATED LINKS</span></span>
