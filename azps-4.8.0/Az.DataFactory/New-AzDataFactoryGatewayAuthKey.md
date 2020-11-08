---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236791"
---
# <span data-ttu-id="5eaa8-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="5eaa8-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="5eaa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5eaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="5eaa8-103">Создает ключ проверки подлинности для шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="5eaa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5eaa8-104">SYNTAX</span></span>

### <span data-ttu-id="5eaa8-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5eaa8-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eaa8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5eaa8-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eaa8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eaa8-107">DESCRIPTION</span></span>
<span data-ttu-id="5eaa8-108">Командлет **New-AzDataFactoryGatewayAuthKey** создает ключ проверки подлинности шлюза для указанного шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="5eaa8-109">Для регистрации шлюза в облачной службе используется этот ключ.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="5eaa8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5eaa8-110">EXAMPLES</span></span>

### <span data-ttu-id="5eaa8-111">Пример 1: создание ключа проверки подлинности шлюза для key1</span><span class="sxs-lookup"><span data-stu-id="5eaa8-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="5eaa8-112">Эта команда создает ключ проверки подлинности шлюза key1 для шлюза фабрики данных с именем MyGateway.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="5eaa8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5eaa8-113">PARAMETERS</span></span>

### <span data-ttu-id="5eaa8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5eaa8-114">-DataFactoryName</span></span>
<span data-ttu-id="5eaa8-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-115">The data factory name.</span></span>

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

### <span data-ttu-id="5eaa8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eaa8-116">-DefaultProfile</span></span>
<span data-ttu-id="5eaa8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5eaa8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eaa8-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="5eaa8-118">-GatewayName</span></span>
<span data-ttu-id="5eaa8-119">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="5eaa8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eaa8-120">-InputObject</span></span>
<span data-ttu-id="5eaa8-121">Объект фабрики данных</span><span class="sxs-lookup"><span data-stu-id="5eaa8-121">The data factory object</span></span>

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

### <span data-ttu-id="5eaa8-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5eaa8-122">-KeyName</span></span>
<span data-ttu-id="5eaa8-123">Имя ключа проверки подлинности шлюза, который должен быть повторно сформирован, либо "key1", либо "key2".</span><span class="sxs-lookup"><span data-stu-id="5eaa8-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eaa8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eaa8-124">-ResourceGroupName</span></span>
<span data-ttu-id="5eaa8-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-125">The resource group name.</span></span>

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

### <span data-ttu-id="5eaa8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5eaa8-126">-Confirm</span></span>
<span data-ttu-id="5eaa8-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eaa8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eaa8-128">-WhatIf</span></span>
<span data-ttu-id="5eaa8-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5eaa8-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eaa8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eaa8-131">CommonParameters</span></span>
<span data-ttu-id="5eaa8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5eaa8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eaa8-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eaa8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eaa8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5eaa8-134">INPUTS</span></span>

### <span data-ttu-id="5eaa8-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5eaa8-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5eaa8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5eaa8-136">System.String</span></span>

## <span data-ttu-id="5eaa8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eaa8-137">OUTPUTS</span></span>

### <span data-ttu-id="5eaa8-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="5eaa8-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="5eaa8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5eaa8-139">NOTES</span></span>
* <span data-ttu-id="5eaa8-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="5eaa8-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5eaa8-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eaa8-141">RELATED LINKS</span></span>

<span data-ttu-id="5eaa8-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="5eaa8-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>
