---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314063"
---
# <span data-ttu-id="e3b7e-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e3b7e-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="e3b7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b7e-103">Получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="e3b7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3b7e-104">SYNTAX</span></span>

### <span data-ttu-id="e3b7e-105">BySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3b7e-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b7e-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3b7e-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b7e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b7e-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b7e-108">Командлет Get-AzDataFactoryV2 получает сведения о фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="e3b7e-109">Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="e3b7e-110">Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="e3b7e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3b7e-111">EXAMPLES</span></span>

### <span data-ttu-id="e3b7e-112">Пример 1: получение всех фабрик данных</span><span class="sxs-lookup"><span data-stu-id="e3b7e-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="e3b7e-113">Отображает сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="e3b7e-114">Пример 2: получение определенной фабрики данных</span><span class="sxs-lookup"><span data-stu-id="e3b7e-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="e3b7e-115">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="e3b7e-116">Укажите параметр фактического значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="e3b7e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3b7e-117">PARAMETERS</span></span>

### <span data-ttu-id="e3b7e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b7e-118">-DefaultProfile</span></span>
<span data-ttu-id="e3b7e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b7e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3b7e-120">-Name</span></span>
<span data-ttu-id="e3b7e-121">Указывает имя фабрики данных, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="e3b7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3b7e-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e3b7e-124">Этот командлет получает сведения о фабриках данных, относящихся к группе. Этот параметр указывает.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="e3b7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b7e-125">CommonParameters</span></span>
<span data-ttu-id="e3b7e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3b7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b7e-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3b7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b7e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3b7e-128">INPUTS</span></span>

### <span data-ttu-id="e3b7e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b7e-129">System.String</span></span>

## <span data-ttu-id="e3b7e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b7e-130">OUTPUTS</span></span>

### <span data-ttu-id="e3b7e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3b7e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e3b7e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3b7e-132">NOTES</span></span>
<span data-ttu-id="e3b7e-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="e3b7e-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e3b7e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3b7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3b7e-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e3b7e-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="e3b7e-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e3b7e-136">Remove-AzDataFactoryV2</span></span>]()
