---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407500"
---
# <span data-ttu-id="1d340-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1d340-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="1d340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d340-102">SYNOPSIS</span></span>
<span data-ttu-id="1d340-103">Сведения о концентраторах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1d340-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="1d340-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d340-104">SYNTAX</span></span>

### <span data-ttu-id="1d340-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d340-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d340-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1d340-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d340-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d340-107">DESCRIPTION</span></span>
<span data-ttu-id="1d340-108">Для получения сведений о концентраторах в фабрике данных Azure можно получить сведения о **cmdlet Get-AzDataFactoryHub.**</span><span class="sxs-lookup"><span data-stu-id="1d340-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="1d340-109">Если указать имя концентратора, этот cmdlet получит сведения об этом центре.</span><span class="sxs-lookup"><span data-stu-id="1d340-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="1d340-110">Если имя не указано, этот cmdlet получает сведения обо всех концентраторах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1d340-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="1d340-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d340-111">EXAMPLES</span></span>

### <span data-ttu-id="1d340-112">Пример 1. Все концентраторы данных</span><span class="sxs-lookup"><span data-stu-id="1d340-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="1d340-113">Эта команда получает все концентраторы данных в группе ресурсов Azure ADFResourceGroup и фабрике данных ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="1d340-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="1d340-114">Пример 2. Получить определенный центр данных</span><span class="sxs-lookup"><span data-stu-id="1d340-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="1d340-115">Эта команда получает сведения об концентраторе MyDataHub в группе ресурсов Azure ADFResourceGroup и фабрике данных ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="1d340-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="1d340-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d340-116">PARAMETERS</span></span>

### <span data-ttu-id="1d340-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1d340-117">-DataFactory</span></span>
<span data-ttu-id="1d340-118">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="1d340-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1d340-119">Этот cmdlet получает сведения о концентраторах в фабрике данных, указанных этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1d340-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d340-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1d340-120">-DataFactoryName</span></span>
<span data-ttu-id="1d340-121">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1d340-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1d340-122">Этот cmdlet получает сведения о концентраторах в фабрике данных, указанных этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1d340-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d340-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d340-123">-DefaultProfile</span></span>
<span data-ttu-id="1d340-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d340-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d340-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1d340-125">-Name</span></span>
<span data-ttu-id="1d340-126">Указывает имя концентратора, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="1d340-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="1d340-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d340-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d340-128">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1d340-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1d340-129">Этот cmdlet получает сведения о концентраторах, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1d340-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d340-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d340-130">CommonParameters</span></span>
<span data-ttu-id="1d340-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d340-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d340-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d340-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d340-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d340-133">INPUTS</span></span>

### <span data-ttu-id="1d340-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1d340-134">System.String</span></span>

### <span data-ttu-id="1d340-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1d340-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1d340-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d340-136">OUTPUTS</span></span>

### <span data-ttu-id="1d340-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="1d340-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="1d340-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d340-138">NOTES</span></span>
* <span data-ttu-id="1d340-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1d340-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1d340-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d340-140">RELATED LINKS</span></span>

[<span data-ttu-id="1d340-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1d340-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="1d340-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1d340-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


