---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973608"
---
# <span data-ttu-id="914fe-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="914fe-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="914fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="914fe-102">SYNOPSIS</span></span>
<span data-ttu-id="914fe-103">Получить операцию развертывания</span><span class="sxs-lookup"><span data-stu-id="914fe-103">Get deployment operation</span></span>

## <span data-ttu-id="914fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="914fe-104">SYNTAX</span></span>

### <span data-ttu-id="914fe-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="914fe-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="914fe-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="914fe-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="914fe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="914fe-107">DESCRIPTION</span></span>
<span data-ttu-id="914fe-108">С помощью **cmdletation Get-AzDeploymentOperation** выведет список всех операций, которые были частью развертывания, чтобы помочь вам определить и предоставить более подробную информацию об операциях, которые не удалось установить для конкретного развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="914fe-109">В ней также могут быть ответы и содержимое запросов для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="914fe-110">Эти же сведения можно получить в сведениях о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="914fe-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="914fe-111">Чтобы получить запрос и содержимое ответа, в включить этот параметр при отправке развертывания через **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="914fe-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="914fe-112">Он может входить в журнал и выводить секрет, например пароли, используемые в свойствах ресурсов или **операциях listKeys,** которые затем возвращаются при восстановлении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="914fe-113">Подробнее об этом параметре и его в том, как его включить, см. New-AzDeployment и отладку ARM развертываниях шаблонов.</span><span class="sxs-lookup"><span data-stu-id="914fe-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="914fe-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="914fe-114">EXAMPLES</span></span>

### <span data-ttu-id="914fe-115">Пример 1. Получить операции развертывания с именем развертывания</span><span class="sxs-lookup"><span data-stu-id="914fe-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="914fe-116">Получает операцию развертывания с именем "тест" в текущей области действия подписки.</span><span class="sxs-lookup"><span data-stu-id="914fe-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="914fe-117">Пример 2. Получить развертывание и получить операции развертывания</span><span class="sxs-lookup"><span data-stu-id="914fe-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="914fe-118">Эта команда получает "тест" развертывания в текущей области подписки и получает результаты операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="914fe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="914fe-119">PARAMETERS</span></span>

### <span data-ttu-id="914fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914fe-120">-DefaultProfile</span></span>
<span data-ttu-id="914fe-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="914fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="914fe-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="914fe-122">-DeploymentName</span></span>
<span data-ttu-id="914fe-123">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-123">The deployment name.</span></span>

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

### <span data-ttu-id="914fe-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="914fe-124">-DeploymentObject</span></span>
<span data-ttu-id="914fe-125">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-125">The deployment object.</span></span>

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

### <span data-ttu-id="914fe-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="914fe-126">-OperationId</span></span>
<span data-ttu-id="914fe-127">ИД операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="914fe-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="914fe-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="914fe-128">-Pre</span></span>
<span data-ttu-id="914fe-129">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="914fe-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="914fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914fe-130">CommonParameters</span></span>
<span data-ttu-id="914fe-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914fe-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="914fe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914fe-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="914fe-133">INPUTS</span></span>

### <span data-ttu-id="914fe-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="914fe-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="914fe-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="914fe-135">OUTPUTS</span></span>

### <span data-ttu-id="914fe-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="914fe-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="914fe-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="914fe-137">NOTES</span></span>

## <span data-ttu-id="914fe-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="914fe-138">RELATED LINKS</span></span>
