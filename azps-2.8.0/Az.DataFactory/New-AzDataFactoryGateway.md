---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 80d981f4b727d713a5cdc235e9e8ea93d652a358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721496"
---
# <span data-ttu-id="89c90-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89c90-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="89c90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89c90-102">SYNOPSIS</span></span>
<span data-ttu-id="89c90-103">Создание шлюза для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="89c90-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="89c90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89c90-104">SYNTAX</span></span>

### <span data-ttu-id="89c90-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89c90-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c90-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="89c90-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89c90-107">DESCRIPTION</span></span>
<span data-ttu-id="89c90-108">Командлет **New-AzDataFactoryGateway** создает шлюз в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="89c90-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="89c90-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89c90-109">EXAMPLES</span></span>

### <span data-ttu-id="89c90-110">Пример 1: Создание шлюза</span><span class="sxs-lookup"><span data-stu-id="89c90-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="89c90-111">Эта команда создает шлюз с именем ContosoGateway в фабрике данных под названием WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="89c90-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="89c90-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89c90-112">PARAMETERS</span></span>

### <span data-ttu-id="89c90-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="89c90-113">-DataFactory</span></span>
<span data-ttu-id="89c90-114">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="89c90-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="89c90-115">Этот командлет создает шлюз для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="89c90-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89c90-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="89c90-116">-DataFactoryName</span></span>
<span data-ttu-id="89c90-117">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="89c90-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="89c90-118">Этот командлет создает шлюз для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="89c90-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89c90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c90-119">-DefaultProfile</span></span>
<span data-ttu-id="89c90-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89c90-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89c90-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="89c90-121">-Description</span></span>
<span data-ttu-id="89c90-122">Задает описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="89c90-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89c90-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89c90-123">-Name</span></span>
<span data-ttu-id="89c90-124">Указывает имя создаваемого шлюза.</span><span class="sxs-lookup"><span data-stu-id="89c90-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="89c90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c90-125">-ResourceGroupName</span></span>
<span data-ttu-id="89c90-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="89c90-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="89c90-127">Этот командлет создает шлюз, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="89c90-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="89c90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c90-128">CommonParameters</span></span>
<span data-ttu-id="89c90-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89c90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c90-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c90-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89c90-131">INPUTS</span></span>

### <span data-ttu-id="89c90-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="89c90-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="89c90-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89c90-133">System.String</span></span>

## <span data-ttu-id="89c90-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89c90-134">OUTPUTS</span></span>

### <span data-ttu-id="89c90-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89c90-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="89c90-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="89c90-136">NOTES</span></span>
* <span data-ttu-id="89c90-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="89c90-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="89c90-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89c90-138">RELATED LINKS</span></span>

[<span data-ttu-id="89c90-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89c90-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="89c90-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89c90-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


