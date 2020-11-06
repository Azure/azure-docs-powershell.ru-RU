---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 94321cc8f9d42cd4ef26e617426f844b9774b5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564959"
---
# <span data-ttu-id="3fd51-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3fd51-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="3fd51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fd51-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd51-103">Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd51-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fd51-104">SYNTAX</span></span>

### <span data-ttu-id="3fd51-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3fd51-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fd51-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3fd51-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fd51-107">DESCRIPTION</span></span>
<span data-ttu-id="3fd51-108">Командлет **Remove-AzureRmDataFactoryLinkedService** Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd51-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="3fd51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fd51-109">EXAMPLES</span></span>

### <span data-ttu-id="3fd51-110">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="3fd51-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="3fd51-111">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3fd51-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="3fd51-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3fd51-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="3fd51-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fd51-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd51-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="3fd51-114">-DataFactory</span></span>
<span data-ttu-id="3fd51-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3fd51-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3fd51-116">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3fd51-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3fd51-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3fd51-117">-DataFactoryName</span></span>
<span data-ttu-id="3fd51-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3fd51-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3fd51-119">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3fd51-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3fd51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd51-120">-DefaultProfile</span></span>
<span data-ttu-id="3fd51-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3fd51-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fd51-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3fd51-122">-Force</span></span>
<span data-ttu-id="3fd51-123">Указывает на то, что этот командлет удаляет связанную службу без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3fd51-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3fd51-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3fd51-124">-Name</span></span>
<span data-ttu-id="3fd51-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3fd51-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd51-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fd51-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd51-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3fd51-128">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3fd51-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3fd51-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fd51-129">-Confirm</span></span>
<span data-ttu-id="3fd51-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fd51-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd51-131">-WhatIf</span></span>
<span data-ttu-id="3fd51-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fd51-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd51-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fd51-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd51-134">CommonParameters</span></span>
<span data-ttu-id="3fd51-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fd51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd51-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd51-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd51-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fd51-137">INPUTS</span></span>

### <span data-ttu-id="3fd51-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="3fd51-138">None</span></span>
<span data-ttu-id="3fd51-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3fd51-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fd51-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fd51-140">OUTPUTS</span></span>

### <span data-ttu-id="3fd51-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd51-141">System.Boolean</span></span>

## <span data-ttu-id="3fd51-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fd51-142">NOTES</span></span>
* <span data-ttu-id="3fd51-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3fd51-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3fd51-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fd51-144">RELATED LINKS</span></span>

[<span data-ttu-id="3fd51-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3fd51-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="3fd51-146">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="3fd51-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


