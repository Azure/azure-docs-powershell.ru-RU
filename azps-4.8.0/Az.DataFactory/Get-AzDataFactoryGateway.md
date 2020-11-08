---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242534"
---
# <span data-ttu-id="6edb0-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6edb0-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="6edb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6edb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6edb0-103">Получение сведений об логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6edb0-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="6edb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6edb0-104">SYNTAX</span></span>

### <span data-ttu-id="6edb0-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6edb0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6edb0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6edb0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6edb0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6edb0-107">DESCRIPTION</span></span>
<span data-ttu-id="6edb0-108">Командлет **Get-AzDataFactoryGateway** получает сведения о логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6edb0-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="6edb0-109">Если указать имя шлюза, этот командлет получает сведения об этом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="6edb0-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="6edb0-110">Если имя не задано, этот командлет получает сведения обо всех шлюзах для фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6edb0-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="6edb0-111">Если вы хотите добавить локальную службу Microsoft SQL Server в качестве связанной службы в фабрику данных, необходимо установить шлюз на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6edb0-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="6edb0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6edb0-112">EXAMPLES</span></span>

### <span data-ttu-id="6edb0-113">Пример 1: получение всех логических шлюзов в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="6edb0-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="6edb0-114">Эта команда получает сведения обо всех логических шлюзах для фабрики данных с именем WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="6edb0-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="6edb0-115">Пример 2: получение определенного логического шлюза в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="6edb0-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="6edb0-116">Эта команда получает сведения о логическом шлюзе с именем Gateway01 в фабрике данных под названием WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="6edb0-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="6edb0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6edb0-117">PARAMETERS</span></span>

### <span data-ttu-id="6edb0-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="6edb0-118">-DataFactory</span></span>
<span data-ttu-id="6edb0-119">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="6edb0-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6edb0-120">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6edb0-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6edb0-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6edb0-121">-DataFactoryName</span></span>
<span data-ttu-id="6edb0-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6edb0-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6edb0-123">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6edb0-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6edb0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6edb0-124">-DefaultProfile</span></span>
<span data-ttu-id="6edb0-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6edb0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6edb0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6edb0-126">-Name</span></span>
<span data-ttu-id="6edb0-127">Указывает имя логического шлюза, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="6edb0-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="6edb0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6edb0-128">-ResourceGroupName</span></span>
<span data-ttu-id="6edb0-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6edb0-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6edb0-130">Этот командлет получает сведения о логических шлюзах, принадлежащих к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6edb0-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6edb0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6edb0-131">CommonParameters</span></span>
<span data-ttu-id="6edb0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6edb0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6edb0-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6edb0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6edb0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6edb0-134">INPUTS</span></span>

### <span data-ttu-id="6edb0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6edb0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6edb0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6edb0-136">System.String</span></span>

## <span data-ttu-id="6edb0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6edb0-137">OUTPUTS</span></span>

### <span data-ttu-id="6edb0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6edb0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="6edb0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6edb0-139">NOTES</span></span>
* <span data-ttu-id="6edb0-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="6edb0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6edb0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6edb0-141">RELATED LINKS</span></span>

[<span data-ttu-id="6edb0-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6edb0-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="6edb0-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6edb0-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="6edb0-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6edb0-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

