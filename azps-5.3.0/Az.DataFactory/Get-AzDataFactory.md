---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519029"
---
# <span data-ttu-id="6dd7c-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6dd7c-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="6dd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd7c-103">Сведения о фабриках данных.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="6dd7c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6dd7c-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dd7c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd7c-106">Для получения сведений о фабриках данных в группе ресурсов Azure можно получить сведения о подмногового ресурсах **Get-AzDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="6dd7c-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="6dd7c-107">Если указать имя фабрики данных, этот cmdlet получит сведения об этой фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="6dd7c-108">Если имя не указано, этот cmdlet получает сведения обо всех фабриках данных в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="6dd7c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6dd7c-109">EXAMPLES</span></span>

### <span data-ttu-id="6dd7c-110">Пример 1. Все фабрики данных</span><span class="sxs-lookup"><span data-stu-id="6dd7c-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="6dd7c-111">Эта команда отображает сведения обо всех фабриках данных в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="6dd7c-112">Пример 2. Получить определенную фабрику данных</span><span class="sxs-lookup"><span data-stu-id="6dd7c-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="6dd7c-113">Эта команда отображает сведения о фабрике данных с именем WikiADF в подписке для группы ресурсов Скайп с именем ADF, а затем сохраняет ее в $DataFactory переменной.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="6dd7c-114">Укажите *параметр DataFactory* в последующих cmdlets, чтобы использовать фабрику данных, храняную в $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="6dd7c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dd7c-115">PARAMETERS</span></span>

### <span data-ttu-id="6dd7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd7c-116">-DefaultProfile</span></span>
<span data-ttu-id="6dd7c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6dd7c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dd7c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6dd7c-118">-Name</span></span>
<span data-ttu-id="6dd7c-119">Название фабрики данных, сведения о которой нужно получить.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="6dd7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6dd7c-121">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6dd7c-122">Этот cmdlet получает сведения о факторах данных, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6dd7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd7c-123">CommonParameters</span></span>
<span data-ttu-id="6dd7c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd7c-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd7c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd7c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dd7c-126">INPUTS</span></span>

### <span data-ttu-id="6dd7c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6dd7c-127">System.String</span></span>

## <span data-ttu-id="6dd7c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6dd7c-128">OUTPUTS</span></span>

### <span data-ttu-id="6dd7c-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6dd7c-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6dd7c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6dd7c-130">NOTES</span></span>
* <span data-ttu-id="6dd7c-131">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="6dd7c-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6dd7c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dd7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="6dd7c-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6dd7c-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="6dd7c-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="6dd7c-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


