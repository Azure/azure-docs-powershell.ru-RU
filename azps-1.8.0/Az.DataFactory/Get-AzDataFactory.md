---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 12028dfd15ca27f7d57f2ffa55e473c835e0391f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901026"
---
# <span data-ttu-id="5ea6b-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6b-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="5ea6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ea6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea6b-103">Получение сведений о фабриках данных.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="5ea6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ea6b-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ea6b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea6b-106">Командлет **Get-AzDataFactory** получает сведения о фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5ea6b-107">Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5ea6b-108">Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="5ea6b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ea6b-109">EXAMPLES</span></span>

### <span data-ttu-id="5ea6b-110">Пример 1: получение всех фабрик данных</span><span class="sxs-lookup"><span data-stu-id="5ea6b-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="5ea6b-111">Эта команда отображает сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5ea6b-112">Пример 2: получение определенной фабрики данных</span><span class="sxs-lookup"><span data-stu-id="5ea6b-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="5ea6b-113">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5ea6b-114">Укажите параметр *фактического* значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5ea6b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ea6b-115">PARAMETERS</span></span>

### <span data-ttu-id="5ea6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea6b-116">-DefaultProfile</span></span>
<span data-ttu-id="5ea6b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ea6b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ea6b-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ea6b-118">-Name</span></span>
<span data-ttu-id="5ea6b-119">Указывает имя фабрики данных, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea6b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea6b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ea6b-121">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5ea6b-122">Этот командлет получает сведения о фабриках данных, относящихся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea6b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea6b-123">CommonParameters</span></span>
<span data-ttu-id="5ea6b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea6b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea6b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea6b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ea6b-126">INPUTS</span></span>

### <span data-ttu-id="5ea6b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea6b-127">System.String</span></span>

## <span data-ttu-id="5ea6b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ea6b-128">OUTPUTS</span></span>

### <span data-ttu-id="5ea6b-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6b-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5ea6b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ea6b-130">NOTES</span></span>
* <span data-ttu-id="5ea6b-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="5ea6b-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ea6b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ea6b-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ea6b-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6b-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="5ea6b-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5ea6b-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


