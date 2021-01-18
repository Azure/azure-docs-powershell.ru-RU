---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505248"
---
# <span data-ttu-id="64bca-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="64bca-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="64bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bca-102">SYNOPSIS</span></span>
<span data-ttu-id="64bca-103">Развертывание в рамках клиента</span><span class="sxs-lookup"><span data-stu-id="64bca-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="64bca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="64bca-104">SYNTAX</span></span>

### <span data-ttu-id="64bca-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64bca-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64bca-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="64bca-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64bca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64bca-107">DESCRIPTION</span></span>
<span data-ttu-id="64bca-108">С помощью **cmdlet Get-AzTenantDeploymentOperation** выведет список всех операций, которые были частью развертывания в текущей области клиента, чтобы помочь вам определить и предоставить более подробную информацию об операциях, которые не удалось установить для конкретного развертывания.</span><span class="sxs-lookup"><span data-stu-id="64bca-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="64bca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="64bca-109">EXAMPLES</span></span>

### <span data-ttu-id="64bca-110">Пример 1. Получить операции развертывания с именем развертывания</span><span class="sxs-lookup"><span data-stu-id="64bca-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="64bca-111">Возвращает операции развертывания с именем Deploy01 в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="64bca-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="64bca-112">Пример 2. Получить развертывание и получить операции развертывания</span><span class="sxs-lookup"><span data-stu-id="64bca-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="64bca-113">Эта команда получает "Развертывание01" в текущей области клиента и получает операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="64bca-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="64bca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64bca-114">PARAMETERS</span></span>

### <span data-ttu-id="64bca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bca-115">-DefaultProfile</span></span>
<span data-ttu-id="64bca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64bca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64bca-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="64bca-117">-DeploymentName</span></span>
<span data-ttu-id="64bca-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="64bca-118">The deployment name.</span></span>

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

### <span data-ttu-id="64bca-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="64bca-119">-DeploymentObject</span></span>
<span data-ttu-id="64bca-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="64bca-120">The deployment object.</span></span>

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

### <span data-ttu-id="64bca-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="64bca-121">-OperationId</span></span>
<span data-ttu-id="64bca-122">ИД операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="64bca-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="64bca-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="64bca-123">-Pre</span></span>
<span data-ttu-id="64bca-124">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="64bca-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="64bca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bca-125">CommonParameters</span></span>
<span data-ttu-id="64bca-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64bca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bca-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64bca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bca-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64bca-128">INPUTS</span></span>

### <span data-ttu-id="64bca-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="64bca-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="64bca-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64bca-130">OUTPUTS</span></span>

### <span data-ttu-id="64bca-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="64bca-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="64bca-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="64bca-132">NOTES</span></span>

## <span data-ttu-id="64bca-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64bca-133">RELATED LINKS</span></span>
