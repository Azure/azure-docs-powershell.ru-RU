---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734884"
---
# <span data-ttu-id="96d7b-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="96d7b-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="96d7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="96d7b-103">Получение сведений об логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="96d7b-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96d7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96d7b-104">SYNTAX</span></span>

### <span data-ttu-id="96d7b-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96d7b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96d7b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="96d7b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96d7b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96d7b-107">DESCRIPTION</span></span>
<span data-ttu-id="96d7b-108">Командлет **Get-AzureRmDataFactoryGateway** получает сведения о логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="96d7b-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="96d7b-109">Если указать имя шлюза, этот командлет получает сведения об этом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="96d7b-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="96d7b-110">Если имя не задано, этот командлет получает сведения обо всех шлюзах для фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="96d7b-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="96d7b-111">Если вы хотите добавить локальную службу Microsoft SQL Server в качестве связанной службы в фабрику данных, необходимо установить шлюз на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="96d7b-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="96d7b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96d7b-112">EXAMPLES</span></span>

### <span data-ttu-id="96d7b-113">Пример 1: получение всех логических шлюзов в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="96d7b-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="96d7b-114">Эта команда получает сведения обо всех логических шлюзах для фабрики данных с именем WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="96d7b-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="96d7b-115">Пример 2: получение определенного логического шлюза в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="96d7b-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="96d7b-116">Эта команда получает сведения о логическом шлюзе с именем Gateway01 в фабрике данных под названием WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="96d7b-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="96d7b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96d7b-117">PARAMETERS</span></span>

### <span data-ttu-id="96d7b-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="96d7b-118">-DataFactory</span></span>
<span data-ttu-id="96d7b-119">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="96d7b-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="96d7b-120">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="96d7b-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="96d7b-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="96d7b-121">-DataFactoryName</span></span>
<span data-ttu-id="96d7b-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="96d7b-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="96d7b-123">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="96d7b-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="96d7b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96d7b-124">-Name</span></span>
<span data-ttu-id="96d7b-125">Указывает имя логического шлюза, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="96d7b-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="96d7b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d7b-126">-ResourceGroupName</span></span>
<span data-ttu-id="96d7b-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="96d7b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="96d7b-128">Этот командлет получает сведения о логических шлюзах, принадлежащих к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="96d7b-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="96d7b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d7b-129">-DefaultProfile</span></span>
<span data-ttu-id="96d7b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96d7b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96d7b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d7b-131">CommonParameters</span></span>
<span data-ttu-id="96d7b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96d7b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d7b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d7b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d7b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96d7b-134">INPUTS</span></span>

## <span data-ttu-id="96d7b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96d7b-135">OUTPUTS</span></span>

### <span data-ttu-id="96d7b-136">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="96d7b-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="96d7b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="96d7b-137">NOTES</span></span>
* <span data-ttu-id="96d7b-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="96d7b-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="96d7b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96d7b-139">RELATED LINKS</span></span>

[<span data-ttu-id="96d7b-140">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="96d7b-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="96d7b-141">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="96d7b-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="96d7b-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="96d7b-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


