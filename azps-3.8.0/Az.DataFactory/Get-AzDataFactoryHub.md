---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074260"
---
# <span data-ttu-id="34438-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="34438-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="34438-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34438-102">SYNOPSIS</span></span>
<span data-ttu-id="34438-103">Получение сведений о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="34438-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="34438-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34438-104">SYNTAX</span></span>

### <span data-ttu-id="34438-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34438-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34438-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34438-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34438-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34438-107">DESCRIPTION</span></span>
<span data-ttu-id="34438-108">Командлет **Get-AzDataFactoryHub** получает сведения о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="34438-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="34438-109">Если указать имя сервера, этот командлет получает сведения об этом центре.</span><span class="sxs-lookup"><span data-stu-id="34438-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="34438-110">Если имя не задано, этот командлет получает сведения обо всех концентраторах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="34438-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="34438-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34438-111">EXAMPLES</span></span>

### <span data-ttu-id="34438-112">Пример 1: получение всех концентраторов данных</span><span class="sxs-lookup"><span data-stu-id="34438-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="34438-113">Эта команда получает все концентраторы данных в группе ресурсов Azure с именем ADFResourceGroup и фабрики данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="34438-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="34438-114">Пример 2: получение определенного концентратора данных</span><span class="sxs-lookup"><span data-stu-id="34438-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="34438-115">Эта команда получает сведения о концентраторе с именем MyDataHub в группе ресурсов Azure с именем ADFResourceGroup и фабрике данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="34438-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="34438-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34438-116">PARAMETERS</span></span>

### <span data-ttu-id="34438-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="34438-117">-DataFactory</span></span>
<span data-ttu-id="34438-118">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="34438-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="34438-119">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34438-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34438-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="34438-120">-DataFactoryName</span></span>
<span data-ttu-id="34438-121">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="34438-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="34438-122">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34438-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34438-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34438-123">-DefaultProfile</span></span>
<span data-ttu-id="34438-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34438-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34438-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34438-125">-Name</span></span>
<span data-ttu-id="34438-126">Указывает имя центра, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="34438-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34438-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34438-127">-ResourceGroupName</span></span>
<span data-ttu-id="34438-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="34438-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34438-129">Этот командлет получает сведения о концентраторах, относящихся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="34438-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34438-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34438-130">CommonParameters</span></span>
<span data-ttu-id="34438-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34438-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34438-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34438-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34438-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34438-133">INPUTS</span></span>

### <span data-ttu-id="34438-134">System. String</span><span class="sxs-lookup"><span data-stu-id="34438-134">System.String</span></span>

### <span data-ttu-id="34438-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34438-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="34438-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34438-136">OUTPUTS</span></span>

### <span data-ttu-id="34438-137">Microsoft. Azure. Commands. Factoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="34438-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="34438-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="34438-138">NOTES</span></span>
* <span data-ttu-id="34438-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="34438-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34438-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34438-140">RELATED LINKS</span></span>

[<span data-ttu-id="34438-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="34438-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="34438-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="34438-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


