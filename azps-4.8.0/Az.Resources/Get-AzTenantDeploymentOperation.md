---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243345"
---
# <span data-ttu-id="3d022-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="3d022-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="3d022-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d022-102">SYNOPSIS</span></span>
<span data-ttu-id="3d022-103">Операция получения развертывания для развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="3d022-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="3d022-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d022-104">SYNTAX</span></span>

### <span data-ttu-id="3d022-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d022-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d022-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3d022-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d022-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d022-107">DESCRIPTION</span></span>
<span data-ttu-id="3d022-108">Командлет **Get-AzTenantDeploymentOperation** перечисляет все операции, которые были частью развертывания в текущей области клиента, чтобы облегчить поиск и предоставление дополнительных сведений об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d022-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="3d022-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d022-109">EXAMPLES</span></span>

### <span data-ttu-id="3d022-110">Пример 1: получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="3d022-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="3d022-111">Возвращает операции развертывания с именем "Deploy01" в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="3d022-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="3d022-112">Пример 2: получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="3d022-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="3d022-113">Эта команда возвращает развертывание "Deploy01" в текущей области клиента и получение его операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d022-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="3d022-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d022-114">PARAMETERS</span></span>

### <span data-ttu-id="3d022-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d022-115">-ApiVersion</span></span>
<span data-ttu-id="3d022-116">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d022-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d022-117">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="3d022-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3d022-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d022-118">-DefaultProfile</span></span>
<span data-ttu-id="3d022-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d022-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d022-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3d022-120">-DeploymentName</span></span>
<span data-ttu-id="3d022-121">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d022-121">The deployment name.</span></span>

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

### <span data-ttu-id="3d022-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3d022-122">-DeploymentObject</span></span>
<span data-ttu-id="3d022-123">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d022-123">The deployment object.</span></span>

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

### <span data-ttu-id="3d022-124">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="3d022-124">-OperationId</span></span>
<span data-ttu-id="3d022-125">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d022-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="3d022-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d022-126">-Pre</span></span>
<span data-ttu-id="3d022-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="3d022-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3d022-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d022-128">CommonParameters</span></span>
<span data-ttu-id="3d022-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d022-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d022-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d022-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d022-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d022-131">INPUTS</span></span>

### <span data-ttu-id="3d022-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3d022-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3d022-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d022-133">OUTPUTS</span></span>

### <span data-ttu-id="3d022-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="3d022-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="3d022-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d022-135">NOTES</span></span>

## <span data-ttu-id="3d022-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d022-136">RELATED LINKS</span></span>
