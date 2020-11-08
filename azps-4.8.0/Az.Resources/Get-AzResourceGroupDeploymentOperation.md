---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 5a5a1134687a5a08b8f00e383105ad9c0a1a2d4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078050"
---
# <span data-ttu-id="362b2-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="362b2-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="362b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="362b2-102">SYNOPSIS</span></span>
<span data-ttu-id="362b2-103">Получает операцию развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="362b2-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="362b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="362b2-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="362b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="362b2-105">DESCRIPTION</span></span>
<span data-ttu-id="362b2-106">Командлет **Get-AzResourceGroupDeploymentOperation** перечисляет все операции, которые были частью развертывания, чтобы помочь вам найти и получить дополнительные сведения об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="362b2-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="362b2-107">Он также может Показать ответ и содержимое запроса для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="362b2-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="362b2-108">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="362b2-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="362b2-109">Чтобы получить содержимое запроса и ответа, включите параметр при отправке развертывания с помощью **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="362b2-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="362b2-110">Она может потенциально регистрировать и представлять секреты, например пароли, используемые в свойстве ресурса или операциях **listKeys** , которые возвращаются при извлечении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="362b2-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="362b2-111">Дополнительные сведения об этом параметре и инструкции по его включению можно найти в разделе New-AzResourceGroupDeployment и Отладка развертывания шаблонов ARM</span><span class="sxs-lookup"><span data-stu-id="362b2-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="362b2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="362b2-112">EXAMPLES</span></span>

### <span data-ttu-id="362b2-113">Пример 1: Get1</span><span class="sxs-lookup"><span data-stu-id="362b2-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="362b2-114">Возвращает операцию развертывания с именем "тест" в группе ресурсов "тест"</span><span class="sxs-lookup"><span data-stu-id="362b2-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="362b2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="362b2-115">PARAMETERS</span></span>

### <span data-ttu-id="362b2-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="362b2-116">-ApiVersion</span></span>
<span data-ttu-id="362b2-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="362b2-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="362b2-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="362b2-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362b2-119">-DefaultProfile</span></span>
<span data-ttu-id="362b2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="362b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362b2-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="362b2-121">-DeploymentName</span></span>
<span data-ttu-id="362b2-122">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="362b2-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362b2-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="362b2-123">-Pre</span></span>
<span data-ttu-id="362b2-124">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="362b2-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="362b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="362b2-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="362b2-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362b2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="362b2-127">-SubscriptionId</span></span>
<span data-ttu-id="362b2-128">Подписку на использование.</span><span class="sxs-lookup"><span data-stu-id="362b2-128">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="362b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362b2-129">CommonParameters</span></span>
<span data-ttu-id="362b2-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="362b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362b2-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="362b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362b2-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="362b2-132">INPUTS</span></span>

### <span data-ttu-id="362b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="362b2-133">System.String</span></span>

### <span data-ttu-id="362b2-134">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="362b2-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="362b2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="362b2-135">OUTPUTS</span></span>

### <span data-ttu-id="362b2-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="362b2-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="362b2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="362b2-137">NOTES</span></span>

## <span data-ttu-id="362b2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="362b2-138">RELATED LINKS</span></span>