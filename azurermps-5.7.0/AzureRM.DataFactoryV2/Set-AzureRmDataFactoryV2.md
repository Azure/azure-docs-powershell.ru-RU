---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: f0fcfd8a99bd28f01077257e48c0dc9662973751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557388"
---
# <span data-ttu-id="05969-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="05969-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="05969-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05969-102">SYNOPSIS</span></span>
<span data-ttu-id="05969-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="05969-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05969-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05969-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05969-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05969-105">DESCRIPTION</span></span>
<span data-ttu-id="05969-106">Командлет **Set-AzureRmDataFactoryV2** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="05969-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="05969-107">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="05969-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="05969-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05969-108">EXAMPLES</span></span>

### <span data-ttu-id="05969-109">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="05969-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="05969-110">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="05969-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="05969-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05969-111">PARAMETERS</span></span>

### <span data-ttu-id="05969-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05969-112">-DefaultProfile</span></span>
<span data-ttu-id="05969-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05969-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05969-114">-Force</span><span class="sxs-lookup"><span data-stu-id="05969-114">-Force</span></span>
<span data-ttu-id="05969-115">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="05969-115">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05969-116">-Location</span><span class="sxs-lookup"><span data-stu-id="05969-116">-Location</span></span>
<span data-ttu-id="05969-117">Фабрика данных создается в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="05969-117">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="05969-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05969-118">-Name</span></span>
<span data-ttu-id="05969-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="05969-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05969-120">-ResourceGroupName</span></span>
<span data-ttu-id="05969-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05969-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="05969-122">-Tag</span></span>
<span data-ttu-id="05969-123">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="05969-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05969-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05969-124">-Confirm</span></span>
<span data-ttu-id="05969-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05969-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05969-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05969-126">-WhatIf</span></span>
<span data-ttu-id="05969-127">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="05969-127">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05969-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05969-128">CommonParameters</span></span>
<span data-ttu-id="05969-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05969-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05969-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05969-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05969-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05969-131">INPUTS</span></span>

### <span data-ttu-id="05969-132">System. String</span><span class="sxs-lookup"><span data-stu-id="05969-132">System.String</span></span>
<span data-ttu-id="05969-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="05969-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="05969-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05969-134">OUTPUTS</span></span>

### <span data-ttu-id="05969-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="05969-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="05969-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="05969-136">NOTES</span></span>
<span data-ttu-id="05969-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="05969-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="05969-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05969-138">RELATED LINKS</span></span>

[<span data-ttu-id="05969-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="05969-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="05969-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="05969-140">Remove-AzureRmDataFactoryV2</span></span>]()
