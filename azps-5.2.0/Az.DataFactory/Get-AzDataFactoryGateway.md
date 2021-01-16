---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407511"
---
# <span data-ttu-id="92a21-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="92a21-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="92a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a21-102">SYNOPSIS</span></span>
<span data-ttu-id="92a21-103">Сведения о логических шлюзах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="92a21-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="92a21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92a21-104">SYNTAX</span></span>

### <span data-ttu-id="92a21-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92a21-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92a21-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="92a21-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92a21-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92a21-107">DESCRIPTION</span></span>
<span data-ttu-id="92a21-108">Для получения сведений о логических шлюзах в фабрике данных Azure можно получить сведения о **cmdlet Get-AzDataFactoryGateway.**</span><span class="sxs-lookup"><span data-stu-id="92a21-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="92a21-109">Если указать имя шлюза, он будет получать сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="92a21-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="92a21-110">Если имя не указано, этот cmdlet получает сведения обо всех шлюзах для фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="92a21-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="92a21-111">Если вы хотите добавить локальное Microsoft SQL Server в качестве связанной службы для фабрики данных, необходимо установить шлюз на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="92a21-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="92a21-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92a21-112">EXAMPLES</span></span>

### <span data-ttu-id="92a21-113">Пример 1. Получите все логические шлюзы в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="92a21-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="92a21-114">Эта команда получает сведения обо всех логических шлюзах для фабрики данных с именем WikiADF в группе ресурсов ADF.</span><span class="sxs-lookup"><span data-stu-id="92a21-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="92a21-115">Пример 2. Получите определенный логический шлюз в фабрике данных</span><span class="sxs-lookup"><span data-stu-id="92a21-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="92a21-116">Эта команда получает сведения о логическом шлюзе "Шлюз01" в фабрике данных с именем WikiADF в группе ресурсов ADF.</span><span class="sxs-lookup"><span data-stu-id="92a21-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="92a21-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a21-117">PARAMETERS</span></span>

### <span data-ttu-id="92a21-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="92a21-118">-DataFactory</span></span>
<span data-ttu-id="92a21-119">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="92a21-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="92a21-120">Этот cmdlet получает сведения о логических шлюзах в фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="92a21-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="92a21-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="92a21-121">-DataFactoryName</span></span>
<span data-ttu-id="92a21-122">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="92a21-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="92a21-123">Этот cmdlet получает сведения о логических шлюзах в фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="92a21-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="92a21-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a21-124">-DefaultProfile</span></span>
<span data-ttu-id="92a21-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="92a21-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92a21-126">-Name</span><span class="sxs-lookup"><span data-stu-id="92a21-126">-Name</span></span>
<span data-ttu-id="92a21-127">Имя логического шлюза, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="92a21-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="92a21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a21-128">-ResourceGroupName</span></span>
<span data-ttu-id="92a21-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="92a21-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="92a21-130">Этот cmdlet получает сведения о логических шлюзах, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="92a21-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="92a21-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a21-131">CommonParameters</span></span>
<span data-ttu-id="92a21-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a21-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a21-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a21-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a21-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92a21-134">INPUTS</span></span>

### <span data-ttu-id="92a21-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="92a21-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="92a21-136">System.String</span><span class="sxs-lookup"><span data-stu-id="92a21-136">System.String</span></span>

## <span data-ttu-id="92a21-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92a21-137">OUTPUTS</span></span>

### <span data-ttu-id="92a21-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="92a21-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="92a21-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92a21-139">NOTES</span></span>
* <span data-ttu-id="92a21-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="92a21-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="92a21-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92a21-141">RELATED LINKS</span></span>

[<span data-ttu-id="92a21-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="92a21-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="92a21-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="92a21-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="92a21-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="92a21-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

