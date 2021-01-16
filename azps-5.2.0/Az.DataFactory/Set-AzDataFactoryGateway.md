---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394804"
---
# <span data-ttu-id="79f9f-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79f9f-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="79f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="79f9f-103">Задает описание шлюза в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="79f9f-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="79f9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79f9f-104">SYNTAX</span></span>

### <span data-ttu-id="79f9f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79f9f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f9f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="79f9f-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79f9f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79f9f-107">DESCRIPTION</span></span>
<span data-ttu-id="79f9f-108">Для указанного шлюза в фабрике данных Azure заданы инструкции для шлюза **Set-AzDataFactoryGateway.**</span><span class="sxs-lookup"><span data-stu-id="79f9f-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="79f9f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79f9f-109">EXAMPLES</span></span>

### <span data-ttu-id="79f9f-110">Пример 1. Настройка описания шлюза</span><span class="sxs-lookup"><span data-stu-id="79f9f-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="79f9f-111">Эта команда задает описание шлюза ContosoGateway в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="79f9f-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="79f9f-112">Параметр Description определяет новое описание.</span><span class="sxs-lookup"><span data-stu-id="79f9f-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="79f9f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79f9f-113">PARAMETERS</span></span>

### <span data-ttu-id="79f9f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="79f9f-114">-DataFactory</span></span>
<span data-ttu-id="79f9f-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="79f9f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="79f9f-116">Этот cmdlet задает описание шлюза в фабрике данных, заданном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79f9f-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79f9f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79f9f-117">-DataFactoryName</span></span>
<span data-ttu-id="79f9f-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="79f9f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="79f9f-119">Этот cmdlet задает описание шлюза в фабрике данных, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79f9f-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79f9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f9f-120">-DefaultProfile</span></span>
<span data-ttu-id="79f9f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="79f9f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f9f-122">-Description</span><span class="sxs-lookup"><span data-stu-id="79f9f-122">-Description</span></span>
<span data-ttu-id="79f9f-123">Описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="79f9f-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f9f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="79f9f-124">-Name</span></span>
<span data-ttu-id="79f9f-125">Указывает имя шлюза, для которого нужно установить описание.</span><span class="sxs-lookup"><span data-stu-id="79f9f-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="79f9f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f9f-126">-ResourceGroupName</span></span>
<span data-ttu-id="79f9f-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="79f9f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="79f9f-128">Этот cmdlet задает описание шлюза, который принадлежит к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79f9f-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="79f9f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f9f-129">CommonParameters</span></span>
<span data-ttu-id="79f9f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f9f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f9f-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f9f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f9f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79f9f-132">INPUTS</span></span>

### <span data-ttu-id="79f9f-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="79f9f-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="79f9f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="79f9f-134">System.String</span></span>

## <span data-ttu-id="79f9f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79f9f-135">OUTPUTS</span></span>

### <span data-ttu-id="79f9f-136">Microsoft.Azure.Commands.DataFactories.Models.PSDAtaFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79f9f-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="79f9f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79f9f-137">NOTES</span></span>
* <span data-ttu-id="79f9f-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="79f9f-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="79f9f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79f9f-139">RELATED LINKS</span></span>

[<span data-ttu-id="79f9f-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79f9f-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="79f9f-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79f9f-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="79f9f-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79f9f-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


