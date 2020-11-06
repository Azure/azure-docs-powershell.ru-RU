---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557448"
---
# <span data-ttu-id="277b2-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="277b2-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="277b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="277b2-102">SYNOPSIS</span></span>
<span data-ttu-id="277b2-103">Получение сведений о фабриках данных.</span><span class="sxs-lookup"><span data-stu-id="277b2-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="277b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="277b2-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="277b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="277b2-105">DESCRIPTION</span></span>
<span data-ttu-id="277b2-106">Командлет **Get-AzureRmDataFactory** получает сведения о фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="277b2-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="277b2-107">Если вы задаете имя фабрики данных, этот командлет получает сведения о фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="277b2-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="277b2-108">Если имя не задано, этот командлет получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="277b2-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="277b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="277b2-109">EXAMPLES</span></span>

### <span data-ttu-id="277b2-110">Пример 1: получение всех фабрик данных</span><span class="sxs-lookup"><span data-stu-id="277b2-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="277b2-111">Эта команда отображает сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="277b2-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="277b2-112">Пример 2: получение определенной фабрики данных</span><span class="sxs-lookup"><span data-stu-id="277b2-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="277b2-113">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов с именем ADF и сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="277b2-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="277b2-114">Укажите параметр *фактического* значения в последующих командлетах для использования фабрики данных, хранящейся в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="277b2-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="277b2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="277b2-115">PARAMETERS</span></span>

### <span data-ttu-id="277b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277b2-116">-DefaultProfile</span></span>
<span data-ttu-id="277b2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="277b2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277b2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="277b2-118">-Name</span></span>
<span data-ttu-id="277b2-119">Указывает имя фабрики данных, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="277b2-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="277b2-121">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="277b2-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="277b2-122">Этот командлет получает сведения о фабриках данных, относящихся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="277b2-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="277b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277b2-123">CommonParameters</span></span>
<span data-ttu-id="277b2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="277b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277b2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277b2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277b2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="277b2-126">INPUTS</span></span>

### <span data-ttu-id="277b2-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="277b2-127">None</span></span>
<span data-ttu-id="277b2-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="277b2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="277b2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="277b2-129">OUTPUTS</span></span>

### <span data-ttu-id="277b2-130">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="277b2-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="277b2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="277b2-131">NOTES</span></span>
* <span data-ttu-id="277b2-132">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="277b2-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="277b2-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="277b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="277b2-134">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="277b2-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="277b2-135">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="277b2-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


