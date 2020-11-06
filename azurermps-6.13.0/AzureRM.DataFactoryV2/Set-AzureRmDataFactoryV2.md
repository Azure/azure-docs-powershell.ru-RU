---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564608"
---
# <span data-ttu-id="1372e-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1372e-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="1372e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1372e-102">SYNOPSIS</span></span>
<span data-ttu-id="1372e-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1372e-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1372e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1372e-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1372e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1372e-105">DESCRIPTION</span></span>
<span data-ttu-id="1372e-106">Командлет **Set-AzureRmDataFactoryV2** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="1372e-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="1372e-107">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1372e-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="1372e-108">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="1372e-108">-- Create linked services.</span></span>
<span data-ttu-id="1372e-109">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="1372e-109">-- Create datasets.</span></span>
<span data-ttu-id="1372e-110">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="1372e-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="1372e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1372e-111">EXAMPLES</span></span>

### <span data-ttu-id="1372e-112">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="1372e-112">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="1372e-113">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="1372e-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="1372e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1372e-114">PARAMETERS</span></span>

### <span data-ttu-id="1372e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1372e-115">-DefaultProfile</span></span>
<span data-ttu-id="1372e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1372e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1372e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1372e-117">-Force</span></span>
<span data-ttu-id="1372e-118">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1372e-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="1372e-119">-Location</span></span>
<span data-ttu-id="1372e-120">Фабрика данных создается в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="1372e-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="1372e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1372e-121">-Name</span></span>
<span data-ttu-id="1372e-122">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1372e-122">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1372e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1372e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1372e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1372e-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1372e-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="1372e-125">-Tag</span></span>
<span data-ttu-id="1372e-126">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1372e-126">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1372e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1372e-127">-Confirm</span></span>
<span data-ttu-id="1372e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1372e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1372e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1372e-129">-WhatIf</span></span>
<span data-ttu-id="1372e-130">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="1372e-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1372e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1372e-131">CommonParameters</span></span>
<span data-ttu-id="1372e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1372e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1372e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1372e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1372e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1372e-134">INPUTS</span></span>

### <span data-ttu-id="1372e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1372e-135">System.String</span></span>

### <span data-ttu-id="1372e-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1372e-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1372e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1372e-137">OUTPUTS</span></span>

### <span data-ttu-id="1372e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1372e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1372e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1372e-139">NOTES</span></span>
<span data-ttu-id="1372e-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="1372e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1372e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1372e-141">RELATED LINKS</span></span>

[<span data-ttu-id="1372e-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1372e-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="1372e-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1372e-143">Remove-AzureRmDataFactoryV2</span></span>]()
