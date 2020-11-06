---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566270"
---
# <span data-ttu-id="ec83d-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec83d-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="ec83d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec83d-102">SYNOPSIS</span></span>
<span data-ttu-id="ec83d-103">Получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ec83d-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec83d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec83d-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="ec83d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec83d-105">DESCRIPTION</span></span>
<span data-ttu-id="ec83d-106">Командлет Get-AzureRmDataFactoryV2 получает сведения о фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ec83d-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="ec83d-107">Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ec83d-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="ec83d-108">Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ec83d-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="ec83d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec83d-109">EXAMPLES</span></span>

### <span data-ttu-id="ec83d-110">Пример 1: получение всех фабрик данных</span><span class="sxs-lookup"><span data-stu-id="ec83d-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="ec83d-111">Отображает сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ec83d-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="ec83d-112">Пример 2: получение определенной фабрики данных</span><span class="sxs-lookup"><span data-stu-id="ec83d-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="ec83d-113">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ec83d-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ec83d-114">Укажите параметр фактического значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ec83d-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="ec83d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec83d-115">PARAMETERS</span></span>

### <span data-ttu-id="ec83d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec83d-116">-Name</span></span>
<span data-ttu-id="ec83d-117">Указывает имя фабрики данных, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ec83d-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec83d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec83d-118">-ResourceGroupName</span></span>
<span data-ttu-id="ec83d-119">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ec83d-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ec83d-120">Этот командлет получает сведения о фабриках данных, относящихся к группе. Этот параметр указывает.</span><span class="sxs-lookup"><span data-stu-id="ec83d-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ec83d-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec83d-121">INPUTS</span></span>

### <span data-ttu-id="ec83d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ec83d-122">System.String</span></span>


## <span data-ttu-id="ec83d-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec83d-123">OUTPUTS</span></span>

### <span data-ttu-id="ec83d-124">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ec83d-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ec83d-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ec83d-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="ec83d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec83d-126">NOTES</span></span>
<span data-ttu-id="ec83d-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ec83d-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ec83d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec83d-128">RELATED LINKS</span></span>
[<span data-ttu-id="ec83d-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec83d-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="ec83d-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec83d-130">Remove-AzureRmDataFactoryV2</span></span>]()

