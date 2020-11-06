---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: b781207bae8b967acadf4a9ef3ae50c5ffc9cfef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564963"
---
# <span data-ttu-id="a208a-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a208a-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="a208a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a208a-102">SYNOPSIS</span></span>
<span data-ttu-id="a208a-103">Удаляет шлюз из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a208a-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a208a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a208a-104">SYNTAX</span></span>

### <span data-ttu-id="a208a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a208a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a208a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a208a-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a208a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a208a-107">DESCRIPTION</span></span>
<span data-ttu-id="a208a-108">Командлет **Remove-AzureRmDataFactoryGateway** удаляет указанный шлюз из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a208a-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="a208a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a208a-109">EXAMPLES</span></span>

### <span data-ttu-id="a208a-110">Пример 1: Удаление шлюза</span><span class="sxs-lookup"><span data-stu-id="a208a-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="a208a-111">Эта команда удаляет шлюз с именем ContosoGateway из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a208a-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="a208a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a208a-112">PARAMETERS</span></span>

### <span data-ttu-id="a208a-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a208a-113">-DataFactory</span></span>
<span data-ttu-id="a208a-114">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a208a-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a208a-115">Этот командлет удаляет шлюз из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a208a-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a208a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a208a-116">-DataFactoryName</span></span>
<span data-ttu-id="a208a-117">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a208a-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a208a-118">Этот командлет удаляет шлюз из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a208a-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a208a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a208a-119">-DefaultProfile</span></span>
<span data-ttu-id="a208a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a208a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a208a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a208a-121">-Force</span></span>
<span data-ttu-id="a208a-122">Указывает на то, что этот командлет удаляет шлюз без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a208a-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a208a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a208a-123">-Name</span></span>
<span data-ttu-id="a208a-124">Указывает имя шлюза, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a208a-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="a208a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a208a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a208a-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a208a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a208a-127">Этот командлет удаляет шлюз, принадлежащий к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a208a-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a208a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a208a-128">-Confirm</span></span>
<span data-ttu-id="a208a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a208a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a208a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a208a-130">-WhatIf</span></span>
<span data-ttu-id="a208a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a208a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a208a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a208a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a208a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a208a-133">CommonParameters</span></span>
<span data-ttu-id="a208a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a208a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a208a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a208a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a208a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a208a-136">INPUTS</span></span>

### <span data-ttu-id="a208a-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="a208a-137">None</span></span>
<span data-ttu-id="a208a-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a208a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a208a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a208a-139">OUTPUTS</span></span>

### <span data-ttu-id="a208a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a208a-140">System.Boolean</span></span>

## <span data-ttu-id="a208a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a208a-141">NOTES</span></span>
* <span data-ttu-id="a208a-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a208a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a208a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a208a-143">RELATED LINKS</span></span>

[<span data-ttu-id="a208a-144">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a208a-144">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="a208a-145">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a208a-145">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="a208a-146">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a208a-146">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


