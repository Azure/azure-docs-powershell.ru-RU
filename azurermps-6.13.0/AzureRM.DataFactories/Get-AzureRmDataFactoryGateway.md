---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 401a72732c59a6dbcdb23c3df1a2f57e5f016315
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568203"
---
# <span data-ttu-id="ac84e-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ac84e-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="ac84e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac84e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac84e-103">Получение сведений об логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ac84e-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac84e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac84e-104">SYNTAX</span></span>

### <span data-ttu-id="ac84e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac84e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac84e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ac84e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac84e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac84e-107">DESCRIPTION</span></span>
<span data-ttu-id="ac84e-108">Командлет **Get-AzureRmDataFactoryGateway** получает сведения о логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ac84e-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="ac84e-109">Если указать имя шлюза, этот командлет получает сведения об этом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="ac84e-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="ac84e-110">Если имя не задано, этот командлет получает сведения обо всех шлюзах для фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ac84e-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="ac84e-111">Если вы хотите добавить локальную службу Microsoft SQL Server в качестве связанной службы в фабрику данных, необходимо установить шлюз на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ac84e-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="ac84e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac84e-112">EXAMPLES</span></span>

### <span data-ttu-id="ac84e-113">Пример 1: получение всех логических шлюзов в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="ac84e-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="ac84e-114">Эта команда получает сведения обо всех логических шлюзах для фабрики данных с именем WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="ac84e-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="ac84e-115">Пример 2: получение определенного логического шлюза в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="ac84e-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="ac84e-116">Эта команда получает сведения о логическом шлюзе с именем Gateway01 в фабрике данных под названием WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="ac84e-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="ac84e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac84e-117">PARAMETERS</span></span>

### <span data-ttu-id="ac84e-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="ac84e-118">-DataFactory</span></span>
<span data-ttu-id="ac84e-119">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ac84e-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ac84e-120">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac84e-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac84e-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac84e-121">-DataFactoryName</span></span>
<span data-ttu-id="ac84e-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ac84e-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac84e-123">Этот командлет получает сведения о логических шлюзах в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac84e-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac84e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac84e-124">-DefaultProfile</span></span>
<span data-ttu-id="ac84e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ac84e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac84e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac84e-126">-Name</span></span>
<span data-ttu-id="ac84e-127">Указывает имя логического шлюза, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="ac84e-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="ac84e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac84e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac84e-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac84e-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac84e-130">Этот командлет получает сведения о логических шлюзах, принадлежащих к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac84e-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac84e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac84e-131">CommonParameters</span></span>
<span data-ttu-id="ac84e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac84e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac84e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac84e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac84e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac84e-134">INPUTS</span></span>

### <span data-ttu-id="ac84e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac84e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ac84e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ac84e-136">System.String</span></span>

## <span data-ttu-id="ac84e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac84e-137">OUTPUTS</span></span>

### <span data-ttu-id="ac84e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ac84e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="ac84e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac84e-139">NOTES</span></span>
* <span data-ttu-id="ac84e-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ac84e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac84e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac84e-141">RELATED LINKS</span></span>

[<span data-ttu-id="ac84e-142">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ac84e-142">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="ac84e-143">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ac84e-143">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="ac84e-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ac84e-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


