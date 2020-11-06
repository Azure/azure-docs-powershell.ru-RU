---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 0e6940a49e4b3a284643bd9353d579213b793d2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565254"
---
# <span data-ttu-id="3e8f9-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="3e8f9-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="3e8f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e8f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8f9-103">Создает ключ проверки подлинности для шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e8f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e8f9-104">SYNTAX</span></span>

### <span data-ttu-id="3e8f9-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e8f9-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e8f9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e8f9-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e8f9-107">DESCRIPTION</span></span>
<span data-ttu-id="3e8f9-108">Командлет **New-AzureRmDataFactoryGatewayAuthKey** создает ключ проверки подлинности шлюза для указанного шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="3e8f9-109">Для регистрации шлюза в облачной службе используется этот ключ.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="3e8f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e8f9-110">EXAMPLES</span></span>

### <span data-ttu-id="3e8f9-111">Пример 1: создание ключа проверки подлинности шлюза для key1</span><span class="sxs-lookup"><span data-stu-id="3e8f9-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="3e8f9-112">Эта команда создает ключ проверки подлинности шлюза key1 для шлюза фабрики данных с именем MyGateway.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="3e8f9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e8f9-113">PARAMETERS</span></span>

### <span data-ttu-id="3e8f9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e8f9-114">-DataFactoryName</span></span>
<span data-ttu-id="3e8f9-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-115">The data factory name.</span></span>

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

### <span data-ttu-id="3e8f9-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="3e8f9-116">-GatewayName</span></span>
<span data-ttu-id="3e8f9-117">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-117">The data factory gateway name.</span></span>

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

### <span data-ttu-id="3e8f9-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3e8f9-118">-KeyName</span></span>
<span data-ttu-id="3e8f9-119">Имя ключа проверки подлинности шлюза, который должен быть повторно сформирован, либо "key1", либо "key2".</span><span class="sxs-lookup"><span data-stu-id="3e8f9-119">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e8f9-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-121">The resource group name.</span></span>

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

### <span data-ttu-id="3e8f9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e8f9-122">-Confirm</span></span>
<span data-ttu-id="3e8f9-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8f9-124">-DefaultProfile</span></span>
<span data-ttu-id="3e8f9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e8f9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e8f9-126">-InputObject</span></span>
<span data-ttu-id="3e8f9-127">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-127">The data factory object.</span></span>

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

### <span data-ttu-id="3e8f9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8f9-128">-WhatIf</span></span>
<span data-ttu-id="3e8f9-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e8f9-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e8f9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8f9-131">CommonParameters</span></span>
<span data-ttu-id="3e8f9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e8f9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8f9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e8f9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8f9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e8f9-134">INPUTS</span></span>

### <span data-ttu-id="3e8f9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e8f9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="3e8f9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3e8f9-136">System.String</span></span>

## <span data-ttu-id="3e8f9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e8f9-137">OUTPUTS</span></span>

### <span data-ttu-id="3e8f9-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="3e8f9-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="3e8f9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e8f9-139">NOTES</span></span>
* <span data-ttu-id="3e8f9-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3e8f9-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e8f9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e8f9-141">RELATED LINKS</span></span>

<span data-ttu-id="3e8f9-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="3e8f9-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

