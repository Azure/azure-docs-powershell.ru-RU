---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245907"
---
# <span data-ttu-id="8e0b2-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8e0b2-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="8e0b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0b2-103">Операция получения развертывания</span><span class="sxs-lookup"><span data-stu-id="8e0b2-103">Get deployment operation</span></span>

## <span data-ttu-id="8e0b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e0b2-104">SYNTAX</span></span>

### <span data-ttu-id="8e0b2-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e0b2-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e0b2-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8e0b2-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e0b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e0b2-107">DESCRIPTION</span></span>
<span data-ttu-id="8e0b2-108">Командлет **Get-AzDeploymentOperation** перечисляет все операции, которые были частью развертывания, чтобы помочь вам найти и получить дополнительные сведения об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="8e0b2-109">Он также может Показать ответ и содержимое запроса для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="8e0b2-110">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="8e0b2-111">Чтобы получить содержимое запроса и ответа, включите параметр при отправке развертывания с помощью **New-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="8e0b2-112">Она может потенциально регистрировать и представлять секреты, например пароли, используемые в свойстве ресурса или операциях **listKeys** , которые возвращаются при извлечении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="8e0b2-113">Дополнительные сведения об этом параметре и инструкции по его включению можно найти в разделе New-AzDeployment и Отладка развертывания шаблонов ARM</span><span class="sxs-lookup"><span data-stu-id="8e0b2-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="8e0b2-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e0b2-114">EXAMPLES</span></span>

### <span data-ttu-id="8e0b2-115">Пример 1: получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="8e0b2-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="8e0b2-116">Возвращает операцию развертывания с именем Test в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="8e0b2-117">Пример 2: получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="8e0b2-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="8e0b2-118">Эта команда возвращает "тест" в текущей области подписки и получение ее операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="8e0b2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e0b2-119">PARAMETERS</span></span>

### <span data-ttu-id="8e0b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0b2-120">-DefaultProfile</span></span>
<span data-ttu-id="8e0b2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e0b2-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8e0b2-122">-DeploymentName</span></span>
<span data-ttu-id="8e0b2-123">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-123">The deployment name.</span></span>

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

### <span data-ttu-id="8e0b2-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8e0b2-124">-DeploymentObject</span></span>
<span data-ttu-id="8e0b2-125">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-125">The deployment object.</span></span>

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

### <span data-ttu-id="8e0b2-126">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="8e0b2-126">-OperationId</span></span>
<span data-ttu-id="8e0b2-127">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="8e0b2-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e0b2-128">-Pre</span></span>
<span data-ttu-id="8e0b2-129">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8e0b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0b2-130">CommonParameters</span></span>
<span data-ttu-id="8e0b2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e0b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0b2-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e0b2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0b2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e0b2-133">INPUTS</span></span>

### <span data-ttu-id="8e0b2-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8e0b2-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8e0b2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e0b2-135">OUTPUTS</span></span>

### <span data-ttu-id="8e0b2-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8e0b2-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="8e0b2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e0b2-137">NOTES</span></span>

## <span data-ttu-id="8e0b2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e0b2-138">RELATED LINKS</span></span>
