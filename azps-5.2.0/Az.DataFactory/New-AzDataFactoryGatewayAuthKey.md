---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324536"
---
# <span data-ttu-id="54255-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="54255-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="54255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54255-102">SYNOPSIS</span></span>
<span data-ttu-id="54255-103">Создает ключ для шлюза фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="54255-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="54255-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54255-104">SYNTAX</span></span>

### <span data-ttu-id="54255-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54255-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54255-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="54255-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54255-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54255-107">DESCRIPTION</span></span>
<span data-ttu-id="54255-108">Для указанного шлюза фабрики данных Azure создается ключ автоостереги шлюза **New-AzDataFactoryGatewayAuthKey.**</span><span class="sxs-lookup"><span data-stu-id="54255-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="54255-109">С помощью этого ключа можно зарегистрировать шлюз в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="54255-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="54255-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54255-110">EXAMPLES</span></span>

### <span data-ttu-id="54255-111">Пример 1. Создание ключа auth шлюза для ключа 1</span><span class="sxs-lookup"><span data-stu-id="54255-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="54255-112">Эта команда создает ключ политики безопасности шлюза Key1 для шлюза фабрики данных MyGateway.</span><span class="sxs-lookup"><span data-stu-id="54255-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="54255-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54255-113">PARAMETERS</span></span>

### <span data-ttu-id="54255-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="54255-114">-DataFactoryName</span></span>
<span data-ttu-id="54255-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="54255-115">The data factory name.</span></span>

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

### <span data-ttu-id="54255-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54255-116">-DefaultProfile</span></span>
<span data-ttu-id="54255-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54255-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54255-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="54255-118">-GatewayName</span></span>
<span data-ttu-id="54255-119">Имя шлюза фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="54255-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="54255-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54255-120">-InputObject</span></span>
<span data-ttu-id="54255-121">Объект фабрики данных</span><span class="sxs-lookup"><span data-stu-id="54255-121">The data factory object</span></span>

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

### <span data-ttu-id="54255-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="54255-122">-KeyName</span></span>
<span data-ttu-id="54255-123">Имя сгенерированного ключа поглинета шлюза: "ключ1" или "ключ2".</span><span class="sxs-lookup"><span data-stu-id="54255-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="54255-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54255-124">-ResourceGroupName</span></span>
<span data-ttu-id="54255-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54255-125">The resource group name.</span></span>

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

### <span data-ttu-id="54255-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54255-126">-Confirm</span></span>
<span data-ttu-id="54255-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54255-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54255-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54255-128">-WhatIf</span></span>
<span data-ttu-id="54255-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54255-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54255-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54255-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54255-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54255-131">CommonParameters</span></span>
<span data-ttu-id="54255-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54255-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54255-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54255-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54255-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54255-134">INPUTS</span></span>

### <span data-ttu-id="54255-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="54255-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="54255-136">System.String</span><span class="sxs-lookup"><span data-stu-id="54255-136">System.String</span></span>

## <span data-ttu-id="54255-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54255-137">OUTPUTS</span></span>

### <span data-ttu-id="54255-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="54255-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="54255-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54255-139">NOTES</span></span>
* <span data-ttu-id="54255-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="54255-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="54255-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54255-141">RELATED LINKS</span></span>

<span data-ttu-id="54255-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="54255-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

