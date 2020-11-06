---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 5239f2143eefe40b777ad1077bbd26d6d645754c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559112"
---
# <span data-ttu-id="9c755-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9c755-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="9c755-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c755-102">SYNOPSIS</span></span>
<span data-ttu-id="9c755-103">Задает описание шлюза в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9c755-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c755-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c755-104">SYNTAX</span></span>

### <span data-ttu-id="9c755-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c755-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c755-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9c755-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c755-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c755-107">DESCRIPTION</span></span>
<span data-ttu-id="9c755-108">Командлет **Set-AzureRmDataFactoryGateway** задает описание указанного шлюза в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9c755-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9c755-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c755-109">EXAMPLES</span></span>

### <span data-ttu-id="9c755-110">Пример 1: Установка описания для шлюза</span><span class="sxs-lookup"><span data-stu-id="9c755-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="9c755-111">Эта команда задает описание шлюза с именем ContosoGateway в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9c755-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="9c755-112">Параметр Description задает новое описание.</span><span class="sxs-lookup"><span data-stu-id="9c755-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="9c755-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c755-113">PARAMETERS</span></span>

### <span data-ttu-id="9c755-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="9c755-114">-DataFactory</span></span>
<span data-ttu-id="9c755-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9c755-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9c755-116">Этот командлет задает описание шлюза в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c755-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9c755-117">-DataFactoryName</span></span>
<span data-ttu-id="9c755-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9c755-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9c755-119">Этот командлет задает описание шлюза в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c755-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c755-120">-DefaultProfile</span></span>
<span data-ttu-id="9c755-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c755-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="9c755-122">-Description</span></span>
<span data-ttu-id="9c755-123">Задает описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="9c755-123">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c755-124">-Name</span></span>
<span data-ttu-id="9c755-125">Указывает имя шлюза, для которого нужно задать описание.</span><span class="sxs-lookup"><span data-stu-id="9c755-125">Specifies the name of the gateway for which to set a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c755-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c755-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9c755-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9c755-128">Этот командлет задает описание шлюза, относящегося к группе, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c755-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c755-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c755-129">CommonParameters</span></span>
<span data-ttu-id="9c755-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c755-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c755-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c755-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c755-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c755-132">INPUTS</span></span>

### <span data-ttu-id="9c755-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c755-133">None</span></span>
<span data-ttu-id="9c755-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c755-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c755-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c755-135">OUTPUTS</span></span>

### <span data-ttu-id="9c755-136">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9c755-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9c755-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c755-137">NOTES</span></span>
* <span data-ttu-id="9c755-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="9c755-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9c755-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c755-139">RELATED LINKS</span></span>

[<span data-ttu-id="9c755-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9c755-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="9c755-141">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9c755-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="9c755-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9c755-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


