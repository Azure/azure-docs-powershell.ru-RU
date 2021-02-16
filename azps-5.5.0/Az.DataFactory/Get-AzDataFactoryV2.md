---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238323"
---
# <span data-ttu-id="5bb81-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5bb81-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="5bb81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bb81-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb81-103">Получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5bb81-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="5bb81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bb81-104">SYNTAX</span></span>

### <span data-ttu-id="5bb81-105">BySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5bb81-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bb81-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="5bb81-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bb81-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bb81-107">DESCRIPTION</span></span>
<span data-ttu-id="5bb81-108">Этот Get-AzDataFactoryV2 получает сведения о фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb81-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5bb81-109">Если указать имя фабрики данных, этот cmdlet получит сведения об этой фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5bb81-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5bb81-110">Если имя не указано, этот cmdlet получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb81-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="5bb81-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bb81-111">EXAMPLES</span></span>

### <span data-ttu-id="5bb81-112">Пример 1. Все фабрики данных</span><span class="sxs-lookup"><span data-stu-id="5bb81-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded
```

<span data-ttu-id="5bb81-113">Выводит сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb81-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5bb81-114">Пример 2. Получить определенную фабрику данных</span><span class="sxs-lookup"><span data-stu-id="5bb81-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="5bb81-115">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов Скайп с именем ADF, а затем сохраняет ее в $DataFactory переменной.</span><span class="sxs-lookup"><span data-stu-id="5bb81-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5bb81-116">Укажите параметр DataFactory в последующих cmdlets, чтобы использовать фабрику данных, храняную в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5bb81-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5bb81-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bb81-117">PARAMETERS</span></span>

### <span data-ttu-id="5bb81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb81-118">-DefaultProfile</span></span>
<span data-ttu-id="5bb81-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bb81-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5bb81-120">-Name</span></span>
<span data-ttu-id="5bb81-121">Название фабрики данных, сведения о которой нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5bb81-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb81-122">-ResourceGroupName</span></span>
<span data-ttu-id="5bb81-123">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb81-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5bb81-124">Этот cmdlet получает сведения о фабриках данных, которые относятся к группе, указанной в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="5bb81-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb81-125">CommonParameters</span></span>
<span data-ttu-id="5bb81-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb81-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bb81-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb81-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bb81-128">INPUTS</span></span>

### <span data-ttu-id="5bb81-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5bb81-129">System.String</span></span>

## <span data-ttu-id="5bb81-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bb81-130">OUTPUTS</span></span>

### <span data-ttu-id="5bb81-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5bb81-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5bb81-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bb81-132">NOTES</span></span>
<span data-ttu-id="5bb81-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="5bb81-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5bb81-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bb81-134">RELATED LINKS</span></span>

[<span data-ttu-id="5bb81-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5bb81-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="5bb81-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5bb81-136">Remove-AzDataFactoryV2</span></span>]()

