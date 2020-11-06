---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9de30d10b34cf666b040c1b25b84e4afeae63a10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569588"
---
# <span data-ttu-id="c64fa-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="c64fa-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="c64fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c64fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c64fa-103">Возвращает ключ проверки подлинности шлюза для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c64fa-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c64fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c64fa-104">SYNTAX</span></span>

### <span data-ttu-id="c64fa-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c64fa-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c64fa-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c64fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c64fa-107">DESCRIPTION</span></span>
<span data-ttu-id="c64fa-108">Командлет **Get-AzureRmDataFactoryGatewayAuthKey** получает ключ проверки подлинности шлюза для указанного шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c64fa-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="c64fa-109">Для регистрации шлюза в облачной службе используется этот ключ проверки подлинности (key1 или key2).</span><span class="sxs-lookup"><span data-stu-id="c64fa-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="c64fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c64fa-110">EXAMPLES</span></span>

### <span data-ttu-id="c64fa-111">Пример 1: получение ключа проверки подлинности шлюза</span><span class="sxs-lookup"><span data-stu-id="c64fa-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="c64fa-112">Эта команда получает ключ проверки подлинности шлюза для шлюза фабрики данных с именем MyGateway.</span><span class="sxs-lookup"><span data-stu-id="c64fa-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="c64fa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c64fa-113">PARAMETERS</span></span>

### <span data-ttu-id="c64fa-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c64fa-114">-DataFactoryName</span></span>
<span data-ttu-id="c64fa-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c64fa-115">The data factory name.</span></span>

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

### <span data-ttu-id="c64fa-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="c64fa-116">-GatewayName</span></span>
<span data-ttu-id="c64fa-117">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c64fa-117">The data factory gateway name.</span></span>

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

### <span data-ttu-id="c64fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="c64fa-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c64fa-119">The resource group name.</span></span>

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

### <span data-ttu-id="c64fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64fa-120">-DefaultProfile</span></span>
<span data-ttu-id="c64fa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c64fa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c64fa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c64fa-122">-InputObject</span></span>
<span data-ttu-id="c64fa-123">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c64fa-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c64fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64fa-124">CommonParameters</span></span>
<span data-ttu-id="c64fa-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c64fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64fa-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64fa-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c64fa-127">INPUTS</span></span>

### <span data-ttu-id="c64fa-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c64fa-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="c64fa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c64fa-129">System.String</span></span>

## <span data-ttu-id="c64fa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c64fa-130">OUTPUTS</span></span>

### <span data-ttu-id="c64fa-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="c64fa-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="c64fa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c64fa-132">NOTES</span></span>
* <span data-ttu-id="c64fa-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="c64fa-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c64fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c64fa-134">RELATED LINKS</span></span>

<span data-ttu-id="c64fa-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="c64fa-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

