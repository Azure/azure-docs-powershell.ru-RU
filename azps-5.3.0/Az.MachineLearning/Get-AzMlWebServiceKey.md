---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425644"
---
# <span data-ttu-id="2c6c7-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="2c6c7-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="2c6c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6c7-103">Извлекает ключи веб-службы.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="2c6c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c6c7-104">SYNTAX</span></span>

### <span data-ttu-id="2c6c7-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c6c7-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c6c7-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="2c6c7-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c6c7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6c7-107">DESCRIPTION</span></span>
<span data-ttu-id="2c6c7-108">Ключи доступа для API времени работы веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="2c6c7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c6c7-109">EXAMPLES</span></span>

### <span data-ttu-id="2c6c7-110">Пример 1. Получить ключи для веб-службы, заданной группой и именем ресурса</span><span class="sxs-lookup"><span data-stu-id="2c6c7-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="2c6c7-111">Пример 2. Получить ключи для экземпляра веб-службы</span><span class="sxs-lookup"><span data-stu-id="2c6c7-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="2c6c7-112">$mlService является объектом типа Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="2c6c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c6c7-113">PARAMETERS</span></span>

### <span data-ttu-id="2c6c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6c7-114">-DefaultProfile</span></span>
<span data-ttu-id="2c6c7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c6c7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c6c7-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="2c6c7-116">-MlWebService</span></span>
<span data-ttu-id="2c6c7-117">Имя веб-службы, для которой извлекаются ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2c6c7-118">-Name</span></span>
<span data-ttu-id="2c6c7-119">Имя веб-службы, для которой извлекаются ключи доступа.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c6c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c6c7-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6c7-122">CommonParameters</span></span>
<span data-ttu-id="2c6c7-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c6c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6c7-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6c7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6c7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c6c7-125">INPUTS</span></span>

### <span data-ttu-id="2c6c7-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="2c6c7-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2c6c7-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c6c7-127">OUTPUTS</span></span>

### <span data-ttu-id="2c6c7-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2c6c7-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="2c6c7-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c6c7-129">NOTES</span></span>
<span data-ttu-id="2c6c7-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2c6c7-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2c6c7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c6c7-131">RELATED LINKS</span></span>
