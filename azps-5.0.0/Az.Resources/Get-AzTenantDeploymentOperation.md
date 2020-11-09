---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316383"
---
# <span data-ttu-id="5787c-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5787c-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="5787c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5787c-102">SYNOPSIS</span></span>
<span data-ttu-id="5787c-103">Операция получения развертывания для развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="5787c-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="5787c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5787c-104">SYNTAX</span></span>

### <span data-ttu-id="5787c-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5787c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5787c-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5787c-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5787c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5787c-107">DESCRIPTION</span></span>
<span data-ttu-id="5787c-108">Командлет **Get-AzTenantDeploymentOperation** перечисляет все операции, которые были частью развертывания в текущей области клиента, чтобы облегчить поиск и предоставление дополнительных сведений об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="5787c-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="5787c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5787c-109">EXAMPLES</span></span>

### <span data-ttu-id="5787c-110">Пример 1: получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="5787c-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="5787c-111">Возвращает операции развертывания с именем "Deploy01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="5787c-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="5787c-112">Пример 2: получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="5787c-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="5787c-113">Эта команда возвращает развертывание "Deploy01" в текущей области клиента и получение его операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="5787c-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="5787c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5787c-114">PARAMETERS</span></span>

### <span data-ttu-id="5787c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5787c-115">-DefaultProfile</span></span>
<span data-ttu-id="5787c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5787c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5787c-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5787c-117">-DeploymentName</span></span>
<span data-ttu-id="5787c-118">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="5787c-118">The deployment name.</span></span>

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

### <span data-ttu-id="5787c-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5787c-119">-DeploymentObject</span></span>
<span data-ttu-id="5787c-120">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="5787c-120">The deployment object.</span></span>

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

### <span data-ttu-id="5787c-121">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="5787c-121">-OperationId</span></span>
<span data-ttu-id="5787c-122">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="5787c-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="5787c-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="5787c-123">-Pre</span></span>
<span data-ttu-id="5787c-124">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="5787c-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5787c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5787c-125">CommonParameters</span></span>
<span data-ttu-id="5787c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5787c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5787c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5787c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5787c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5787c-128">INPUTS</span></span>

### <span data-ttu-id="5787c-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5787c-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5787c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5787c-130">OUTPUTS</span></span>

### <span data-ttu-id="5787c-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5787c-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="5787c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5787c-132">NOTES</span></span>

## <span data-ttu-id="5787c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5787c-133">RELATED LINKS</span></span>
