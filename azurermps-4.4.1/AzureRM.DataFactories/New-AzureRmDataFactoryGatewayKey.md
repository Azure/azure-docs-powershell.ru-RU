---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565253"
---
# <span data-ttu-id="ed414-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ed414-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="ed414-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed414-102">SYNOPSIS</span></span>
<span data-ttu-id="ed414-103">Создание ключа шлюза для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ed414-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="ed414-104">Этот командлет устарел, поэтому вместо него следует использовать **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="ed414-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed414-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed414-105">SYNTAX</span></span>

### <span data-ttu-id="ed414-106">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed414-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed414-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ed414-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed414-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed414-108">DESCRIPTION</span></span>
<span data-ttu-id="ed414-109">Командлет **New-AzureRmDataFactoryGatewayKey** создает ключ шлюза для указанного шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ed414-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="ed414-110">Для регистрации шлюза в облачной службе используется этот ключ.</span><span class="sxs-lookup"><span data-stu-id="ed414-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="ed414-111">Этот командлет устарел, поэтому вместо него следует использовать **New-AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="ed414-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="ed414-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed414-112">EXAMPLES</span></span>

### <span data-ttu-id="ed414-113">Пример 1: создание ключа шлюза</span><span class="sxs-lookup"><span data-stu-id="ed414-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="ed414-114">Эта команда создает ключ шлюза для шлюза фабрики данных с именем ContosoGateway, а затем передает ключ шлюза в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ed414-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed414-115">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="ed414-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="ed414-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed414-116">PARAMETERS</span></span>

### <span data-ttu-id="ed414-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="ed414-117">-DataFactory</span></span>
<span data-ttu-id="ed414-118">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ed414-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ed414-119">Этот командлет создает ключ шлюза для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ed414-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed414-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ed414-120">-DataFactoryName</span></span>
<span data-ttu-id="ed414-121">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ed414-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ed414-122">Этот командлет создает ключ шлюза для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ed414-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed414-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ed414-123">-GatewayName</span></span>
<span data-ttu-id="ed414-124">Указывает имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="ed414-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="ed414-125">Этот командлет создает ключ для шлюза, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ed414-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed414-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed414-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed414-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ed414-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ed414-128">Этот командлет создает ключ для шлюза, относящегося к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ed414-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed414-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed414-129">-DefaultProfile</span></span>
<span data-ttu-id="ed414-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed414-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed414-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed414-131">CommonParameters</span></span>
<span data-ttu-id="ed414-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed414-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed414-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed414-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed414-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed414-134">INPUTS</span></span>

## <span data-ttu-id="ed414-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed414-135">OUTPUTS</span></span>

### <span data-ttu-id="ed414-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ed414-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="ed414-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed414-137">NOTES</span></span>
* <span data-ttu-id="ed414-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ed414-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ed414-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed414-139">RELATED LINKS</span></span>

<span data-ttu-id="ed414-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="ed414-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


