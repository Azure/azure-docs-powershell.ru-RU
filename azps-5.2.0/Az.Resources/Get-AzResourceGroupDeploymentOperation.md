---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398151"
---
# <span data-ttu-id="bc721-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bc721-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="bc721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc721-102">SYNOPSIS</span></span>
<span data-ttu-id="bc721-103">Получает операцию развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc721-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="bc721-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc721-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc721-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc721-105">DESCRIPTION</span></span>
<span data-ttu-id="bc721-106">С помощью **cmdletлета Get-AzResourceGroupDeploymentOperation** перечислены все операции, которые были частью развертывания, чтобы помочь вам определить и предоставить более подробную информацию об операциях, которые не удалось сделать в конкретной операции.</span><span class="sxs-lookup"><span data-stu-id="bc721-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="bc721-107">В ней также могут быть ответы и содержимое запросов для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="bc721-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="bc721-108">Эти же сведения можно получить в сведениях о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="bc721-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="bc721-109">Чтобы получить запрос и содержимое ответа, в включить этот параметр при отправке развертывания через **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="bc721-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="bc721-110">Он может входить в журнал и выводить секрет, например пароли, используемые в свойствах ресурсов или **операциях listKeys,** которые затем возвращаются при восстановлении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="bc721-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="bc721-111">Подробнее об этом параметре и его в том, как его включить, см. New-AzResourceGroupDeployment и отладку ARM развертываниях шаблонов.</span><span class="sxs-lookup"><span data-stu-id="bc721-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="bc721-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc721-112">EXAMPLES</span></span>

### <span data-ttu-id="bc721-113">Пример 1. Получить1</span><span class="sxs-lookup"><span data-stu-id="bc721-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="bc721-114">Получает операцию развертывания с названием "тест" в группе ресурсов "тест"</span><span class="sxs-lookup"><span data-stu-id="bc721-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="bc721-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc721-115">PARAMETERS</span></span>

### <span data-ttu-id="bc721-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc721-116">-DefaultProfile</span></span>
<span data-ttu-id="bc721-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc721-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc721-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bc721-118">-DeploymentName</span></span>
<span data-ttu-id="bc721-119">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="bc721-119">The deployment name.</span></span>

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

### <span data-ttu-id="bc721-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="bc721-120">-Pre</span></span>
<span data-ttu-id="bc721-121">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="bc721-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bc721-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc721-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc721-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc721-123">The resource group name.</span></span>

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

### <span data-ttu-id="bc721-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc721-124">-SubscriptionId</span></span>
<span data-ttu-id="bc721-125">Используемая подписка.</span><span class="sxs-lookup"><span data-stu-id="bc721-125">The subscription to use.</span></span>

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

### <span data-ttu-id="bc721-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc721-126">CommonParameters</span></span>
<span data-ttu-id="bc721-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc721-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc721-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc721-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc721-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc721-129">INPUTS</span></span>

### <span data-ttu-id="bc721-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bc721-130">System.String</span></span>

### <span data-ttu-id="bc721-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc721-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bc721-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc721-132">OUTPUTS</span></span>

### <span data-ttu-id="bc721-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bc721-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="bc721-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc721-134">NOTES</span></span>

## <span data-ttu-id="bc721-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc721-135">RELATED LINKS</span></span>
