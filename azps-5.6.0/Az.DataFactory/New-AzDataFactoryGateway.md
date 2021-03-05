---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 04026cf8cc01e1733c44821824ca4b0682b2b66d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974968"
---
# <span data-ttu-id="89119-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89119-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="89119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89119-102">SYNOPSIS</span></span>
<span data-ttu-id="89119-103">Создает шлюз для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="89119-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="89119-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89119-104">SYNTAX</span></span>

### <span data-ttu-id="89119-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89119-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89119-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="89119-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89119-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89119-107">DESCRIPTION</span></span>
<span data-ttu-id="89119-108">Для создания шлюза в фабрике данных Azure **создается cmdlet New-AzDataFactoryGateway.**</span><span class="sxs-lookup"><span data-stu-id="89119-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="89119-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89119-109">EXAMPLES</span></span>

### <span data-ttu-id="89119-110">Пример 1. Создание шлюза</span><span class="sxs-lookup"><span data-stu-id="89119-110">Example 1: Create a gateway</span></span>
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

<span data-ttu-id="89119-111">Эта команда создает шлюз ContosoGateway в фабрике данных с именем WikiADF в группе ресурсов ADF.</span><span class="sxs-lookup"><span data-stu-id="89119-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="89119-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89119-112">PARAMETERS</span></span>

### <span data-ttu-id="89119-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="89119-113">-DataFactory</span></span>
<span data-ttu-id="89119-114">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="89119-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="89119-115">Этот cmdlet создает шлюз для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="89119-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89119-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="89119-116">-DataFactoryName</span></span>
<span data-ttu-id="89119-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="89119-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="89119-118">Этот cmdlet создает шлюз для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="89119-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="89119-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89119-119">-DefaultProfile</span></span>
<span data-ttu-id="89119-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89119-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89119-121">-Description</span><span class="sxs-lookup"><span data-stu-id="89119-121">-Description</span></span>
<span data-ttu-id="89119-122">Описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="89119-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="89119-123">-Name</span><span class="sxs-lookup"><span data-stu-id="89119-123">-Name</span></span>
<span data-ttu-id="89119-124">Указывает имя созда создаемого шлюза.</span><span class="sxs-lookup"><span data-stu-id="89119-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="89119-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89119-125">-ResourceGroupName</span></span>
<span data-ttu-id="89119-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="89119-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="89119-127">Этот cmdlet создает шлюз, который принадлежит к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="89119-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="89119-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89119-128">CommonParameters</span></span>
<span data-ttu-id="89119-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89119-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89119-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89119-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89119-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89119-131">INPUTS</span></span>

### <span data-ttu-id="89119-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="89119-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="89119-133">System.String</span><span class="sxs-lookup"><span data-stu-id="89119-133">System.String</span></span>

## <span data-ttu-id="89119-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89119-134">OUTPUTS</span></span>

### <span data-ttu-id="89119-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89119-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="89119-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89119-136">NOTES</span></span>
* <span data-ttu-id="89119-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="89119-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="89119-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89119-138">RELATED LINKS</span></span>

[<span data-ttu-id="89119-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89119-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="89119-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="89119-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


