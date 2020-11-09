---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313925"
---
# <span data-ttu-id="9230a-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9230a-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9230a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9230a-102">SYNOPSIS</span></span>
<span data-ttu-id="9230a-103">Создание шлюза для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9230a-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="9230a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9230a-104">SYNTAX</span></span>

### <span data-ttu-id="9230a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9230a-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9230a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9230a-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9230a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9230a-107">DESCRIPTION</span></span>
<span data-ttu-id="9230a-108">Командлет **New-AzDataFactoryGateway** создает шлюз в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9230a-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9230a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9230a-109">EXAMPLES</span></span>

### <span data-ttu-id="9230a-110">Пример 1: Создание шлюза</span><span class="sxs-lookup"><span data-stu-id="9230a-110">Example 1: Create a gateway</span></span>
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

<span data-ttu-id="9230a-111">Эта команда создает шлюз с именем ContosoGateway в фабрике данных под названием WikiADF в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="9230a-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="9230a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9230a-112">PARAMETERS</span></span>

### <span data-ttu-id="9230a-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="9230a-113">-DataFactory</span></span>
<span data-ttu-id="9230a-114">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9230a-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9230a-115">Этот командлет создает шлюз для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9230a-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9230a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9230a-116">-DataFactoryName</span></span>
<span data-ttu-id="9230a-117">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9230a-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9230a-118">Этот командлет создает шлюз для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9230a-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9230a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9230a-119">-DefaultProfile</span></span>
<span data-ttu-id="9230a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9230a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9230a-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="9230a-121">-Description</span></span>
<span data-ttu-id="9230a-122">Задает описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="9230a-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="9230a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9230a-123">-Name</span></span>
<span data-ttu-id="9230a-124">Указывает имя создаваемого шлюза.</span><span class="sxs-lookup"><span data-stu-id="9230a-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="9230a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9230a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9230a-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9230a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9230a-127">Этот командлет создает шлюз, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9230a-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9230a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9230a-128">CommonParameters</span></span>
<span data-ttu-id="9230a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9230a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9230a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9230a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9230a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9230a-131">INPUTS</span></span>

### <span data-ttu-id="9230a-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9230a-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9230a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9230a-133">System.String</span></span>

## <span data-ttu-id="9230a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9230a-134">OUTPUTS</span></span>

### <span data-ttu-id="9230a-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9230a-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9230a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9230a-136">NOTES</span></span>
* <span data-ttu-id="9230a-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="9230a-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9230a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9230a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9230a-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9230a-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="9230a-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9230a-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


