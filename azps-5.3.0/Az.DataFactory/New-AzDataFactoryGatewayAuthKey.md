---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518962"
---
# <span data-ttu-id="8ec88-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="8ec88-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="8ec88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec88-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec88-103">Создает ключ для шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec88-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="8ec88-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ec88-104">SYNTAX</span></span>

### <span data-ttu-id="8ec88-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ec88-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ec88-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8ec88-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec88-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ec88-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec88-108">Для указанного шлюза фабрики данных Azure создается ключ проверка безопасности шлюза **New-AzDataFactoryGatewayAuthKey.**</span><span class="sxs-lookup"><span data-stu-id="8ec88-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="8ec88-109">С помощью этого ключа можно зарегистрировать шлюз в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="8ec88-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="8ec88-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ec88-110">EXAMPLES</span></span>

### <span data-ttu-id="8ec88-111">Пример 1. Создание ключа auth шлюза для ключа 1</span><span class="sxs-lookup"><span data-stu-id="8ec88-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="8ec88-112">Эта команда создает ключ строгой защиты шлюза Key1 для шлюза фабрики данных MyGateway.</span><span class="sxs-lookup"><span data-stu-id="8ec88-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="8ec88-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec88-113">PARAMETERS</span></span>

### <span data-ttu-id="8ec88-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8ec88-114">-DataFactoryName</span></span>
<span data-ttu-id="8ec88-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8ec88-115">The data factory name.</span></span>

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

### <span data-ttu-id="8ec88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec88-116">-DefaultProfile</span></span>
<span data-ttu-id="8ec88-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ec88-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ec88-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="8ec88-118">-GatewayName</span></span>
<span data-ttu-id="8ec88-119">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8ec88-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="8ec88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ec88-120">-InputObject</span></span>
<span data-ttu-id="8ec88-121">Объект фабрики данных</span><span class="sxs-lookup"><span data-stu-id="8ec88-121">The data factory object</span></span>

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

### <span data-ttu-id="8ec88-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8ec88-122">-KeyName</span></span>
<span data-ttu-id="8ec88-123">Имя сгенерированной части шлюза (key1 или key2).</span><span class="sxs-lookup"><span data-stu-id="8ec88-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="8ec88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec88-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ec88-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ec88-125">The resource group name.</span></span>

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

### <span data-ttu-id="8ec88-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ec88-126">-Confirm</span></span>
<span data-ttu-id="8ec88-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8ec88-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec88-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec88-128">-WhatIf</span></span>
<span data-ttu-id="8ec88-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec88-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ec88-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ec88-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec88-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec88-131">CommonParameters</span></span>
<span data-ttu-id="8ec88-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec88-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec88-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec88-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec88-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ec88-134">INPUTS</span></span>

### <span data-ttu-id="8ec88-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8ec88-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8ec88-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8ec88-136">System.String</span></span>

## <span data-ttu-id="8ec88-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ec88-137">OUTPUTS</span></span>

### <span data-ttu-id="8ec88-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="8ec88-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="8ec88-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ec88-139">NOTES</span></span>
* <span data-ttu-id="8ec88-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="8ec88-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8ec88-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ec88-141">RELATED LINKS</span></span>

<span data-ttu-id="8ec88-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="8ec88-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

