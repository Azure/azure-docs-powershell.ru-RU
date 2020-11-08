---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074551"
---
# <span data-ttu-id="a2d77-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a2d77-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a2d77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2d77-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d77-103">Возвращает ключ проверки подлинности шлюза для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d77-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="a2d77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2d77-104">SYNTAX</span></span>

### <span data-ttu-id="a2d77-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2d77-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d77-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a2d77-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d77-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2d77-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d77-108">Командлет **Get-AzDataFactoryGatewayAuthKey** получает ключ проверки подлинности шлюза для указанного шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d77-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="a2d77-109">Для регистрации шлюза в облачной службе используется этот ключ проверки подлинности (key1 или key2).</span><span class="sxs-lookup"><span data-stu-id="a2d77-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="a2d77-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2d77-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d77-111">Пример 1: получение ключа проверки подлинности шлюза</span><span class="sxs-lookup"><span data-stu-id="a2d77-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="a2d77-112">Эта команда получает ключ проверки подлинности шлюза для шлюза фабрики данных с именем MyGateway.</span><span class="sxs-lookup"><span data-stu-id="a2d77-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="a2d77-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2d77-113">PARAMETERS</span></span>

### <span data-ttu-id="a2d77-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a2d77-114">-DataFactoryName</span></span>
<span data-ttu-id="a2d77-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a2d77-115">The data factory name.</span></span>

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

### <span data-ttu-id="a2d77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d77-116">-DefaultProfile</span></span>
<span data-ttu-id="a2d77-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2d77-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2d77-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a2d77-118">-GatewayName</span></span>
<span data-ttu-id="a2d77-119">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a2d77-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="a2d77-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d77-120">-InputObject</span></span>
<span data-ttu-id="a2d77-121">Объект фабрики данных</span><span class="sxs-lookup"><span data-stu-id="a2d77-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d77-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d77-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2d77-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2d77-123">The resource group name.</span></span>

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

### <span data-ttu-id="a2d77-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d77-124">CommonParameters</span></span>
<span data-ttu-id="a2d77-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2d77-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d77-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d77-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d77-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2d77-127">INPUTS</span></span>

### <span data-ttu-id="a2d77-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a2d77-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a2d77-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d77-129">System.String</span></span>

## <span data-ttu-id="a2d77-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2d77-130">OUTPUTS</span></span>

### <span data-ttu-id="a2d77-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a2d77-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a2d77-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2d77-132">NOTES</span></span>
* <span data-ttu-id="a2d77-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a2d77-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a2d77-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2d77-134">RELATED LINKS</span></span>

<span data-ttu-id="a2d77-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="a2d77-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

