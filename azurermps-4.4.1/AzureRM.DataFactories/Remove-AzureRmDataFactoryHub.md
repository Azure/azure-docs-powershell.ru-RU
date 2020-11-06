---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 6788f2dea9cf46b888f729ab97640201f740e80d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566289"
---
# <span data-ttu-id="f752f-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f752f-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="f752f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f752f-102">SYNOPSIS</span></span>
<span data-ttu-id="f752f-103">Удаляет концентратор из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f752f-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f752f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f752f-104">SYNTAX</span></span>

### <span data-ttu-id="f752f-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f752f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f752f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f752f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f752f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f752f-107">DESCRIPTION</span></span>
<span data-ttu-id="f752f-108">Командлет **Remove-AzureRmDataFactoryHub** удаляет концентратор из фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="f752f-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="f752f-109">При удалении концентратора также удаляются все связанные службы и конвейеры в центре.</span><span class="sxs-lookup"><span data-stu-id="f752f-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="f752f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f752f-110">EXAMPLES</span></span>

### <span data-ttu-id="f752f-111">Пример 1: удаление концентратора</span><span class="sxs-lookup"><span data-stu-id="f752f-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="f752f-112">Эта команда удаляет концентратор с именем ContosoDataHub из группы ресурсов Azure с именем ADFResourceGroup и фабрики данных под названием ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="f752f-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f752f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f752f-113">PARAMETERS</span></span>

### <span data-ttu-id="f752f-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="f752f-114">-DataFactory</span></span>
<span data-ttu-id="f752f-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f752f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f752f-116">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f752f-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f752f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f752f-117">-DataFactoryName</span></span>
<span data-ttu-id="f752f-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f752f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f752f-119">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f752f-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f752f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f752f-120">-Force</span></span>
<span data-ttu-id="f752f-121">Указывает на то, что этот командлет удаляет концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f752f-121">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f752f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f752f-122">-Name</span></span>
<span data-ttu-id="f752f-123">Указывает имя удаляемого узла.</span><span class="sxs-lookup"><span data-stu-id="f752f-123">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f752f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f752f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f752f-125">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f752f-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f752f-126">Этот командлет удаляет концентратор из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f752f-126">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f752f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f752f-127">-Confirm</span></span>
<span data-ttu-id="f752f-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f752f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f752f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f752f-129">-WhatIf</span></span>
<span data-ttu-id="f752f-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f752f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f752f-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f752f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f752f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f752f-132">-DefaultProfile</span></span>
<span data-ttu-id="f752f-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f752f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f752f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f752f-134">CommonParameters</span></span>
<span data-ttu-id="f752f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f752f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f752f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f752f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f752f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f752f-137">INPUTS</span></span>

## <span data-ttu-id="f752f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f752f-138">OUTPUTS</span></span>

### <span data-ttu-id="f752f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f752f-139">System.Boolean</span></span>

## <span data-ttu-id="f752f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f752f-140">NOTES</span></span>
* <span data-ttu-id="f752f-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="f752f-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f752f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f752f-142">RELATED LINKS</span></span>

[<span data-ttu-id="f752f-143">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f752f-143">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="f752f-144">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f752f-144">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


