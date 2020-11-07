---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: cca0b397f85a0e0fd42f1e3331294881e1e89014
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732025"
---
# <span data-ttu-id="71987-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="71987-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="71987-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71987-102">SYNOPSIS</span></span>
<span data-ttu-id="71987-103">Получение сведений о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="71987-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71987-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71987-104">SYNTAX</span></span>

### <span data-ttu-id="71987-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71987-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71987-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="71987-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71987-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71987-107">DESCRIPTION</span></span>
<span data-ttu-id="71987-108">Командлет **Get-AzureRmDataFactoryHub** получает сведения о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="71987-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="71987-109">Если указать имя сервера, этот командлет получает сведения об этом центре.</span><span class="sxs-lookup"><span data-stu-id="71987-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="71987-110">Если имя не задано, этот командлет получает сведения обо всех концентраторах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="71987-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="71987-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71987-111">EXAMPLES</span></span>

### <span data-ttu-id="71987-112">Пример 1: получение всех концентраторов данных</span><span class="sxs-lookup"><span data-stu-id="71987-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="71987-113">Эта команда получает все концентраторы данных в группе ресурсов Azure с именем ADFResourceGroup и фабрики данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="71987-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="71987-114">Пример 2: получение определенного концентратора данных</span><span class="sxs-lookup"><span data-stu-id="71987-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="71987-115">Эта команда получает сведения о концентраторе с именем MyDataHub в группе ресурсов Azure с именем ADFResourceGroup и фабрике данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="71987-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="71987-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71987-116">PARAMETERS</span></span>

### <span data-ttu-id="71987-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="71987-117">-DataFactory</span></span>
<span data-ttu-id="71987-118">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="71987-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="71987-119">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="71987-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71987-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71987-120">-DataFactoryName</span></span>
<span data-ttu-id="71987-121">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="71987-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="71987-122">Этот командлет получает сведения о концентраторах в фабрике данных, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="71987-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71987-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71987-123">-DefaultProfile</span></span>
<span data-ttu-id="71987-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71987-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71987-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71987-125">-Name</span></span>
<span data-ttu-id="71987-126">Указывает имя центра, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="71987-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71987-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71987-127">-ResourceGroupName</span></span>
<span data-ttu-id="71987-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="71987-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="71987-129">Этот командлет получает сведения о концентраторах, относящихся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="71987-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71987-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71987-130">CommonParameters</span></span>
<span data-ttu-id="71987-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71987-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71987-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71987-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71987-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71987-133">INPUTS</span></span>

### <span data-ttu-id="71987-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="71987-134">None</span></span>
<span data-ttu-id="71987-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="71987-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71987-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71987-136">OUTPUTS</span></span>

### <span data-ttu-id="71987-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. factors. Models. PSHub]</span><span class="sxs-lookup"><span data-stu-id="71987-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="71987-138">Microsoft. Azure. Commands. Factoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="71987-138">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="71987-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="71987-139">NOTES</span></span>
* <span data-ttu-id="71987-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="71987-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="71987-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71987-141">RELATED LINKS</span></span>

[<span data-ttu-id="71987-142">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="71987-142">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="71987-143">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="71987-143">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


