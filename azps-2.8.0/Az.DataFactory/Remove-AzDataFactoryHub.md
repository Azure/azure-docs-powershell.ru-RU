---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721476"
---
# <span data-ttu-id="9347c-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9347c-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="9347c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9347c-102">SYNOPSIS</span></span>
<span data-ttu-id="9347c-103">Удаляет концентратор из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9347c-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="9347c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9347c-104">SYNTAX</span></span>

### <span data-ttu-id="9347c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9347c-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9347c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9347c-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9347c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9347c-107">DESCRIPTION</span></span>
<span data-ttu-id="9347c-108">Командлет **Remove-AzDataFactoryHub** удаляет концентратор из фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="9347c-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="9347c-109">При удалении концентратора также удаляются все связанные службы и конвейеры в центре.</span><span class="sxs-lookup"><span data-stu-id="9347c-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="9347c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9347c-110">EXAMPLES</span></span>

### <span data-ttu-id="9347c-111">Пример 1: удаление концентратора</span><span class="sxs-lookup"><span data-stu-id="9347c-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="9347c-112">Эта команда удаляет концентратор с именем ContosoDataHub из группы ресурсов Azure с именем ADFResourceGroup и фабрики данных под названием ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="9347c-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="9347c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9347c-113">PARAMETERS</span></span>

### <span data-ttu-id="9347c-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="9347c-114">-DataFactory</span></span>
<span data-ttu-id="9347c-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9347c-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9347c-116">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9347c-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9347c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9347c-117">-DataFactoryName</span></span>
<span data-ttu-id="9347c-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9347c-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9347c-119">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9347c-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9347c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9347c-120">-DefaultProfile</span></span>
<span data-ttu-id="9347c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9347c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9347c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9347c-122">-Force</span></span>
<span data-ttu-id="9347c-123">Указывает на то, что этот командлет удаляет концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9347c-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9347c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9347c-124">-Name</span></span>
<span data-ttu-id="9347c-125">Указывает имя удаляемого узла.</span><span class="sxs-lookup"><span data-stu-id="9347c-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="9347c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9347c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9347c-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9347c-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9347c-128">Этот командлет удаляет концентратор из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9347c-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9347c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9347c-129">-Confirm</span></span>
<span data-ttu-id="9347c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9347c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9347c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9347c-131">-WhatIf</span></span>
<span data-ttu-id="9347c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9347c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9347c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9347c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9347c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9347c-134">CommonParameters</span></span>
<span data-ttu-id="9347c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9347c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9347c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9347c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9347c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9347c-137">INPUTS</span></span>

### <span data-ttu-id="9347c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9347c-138">System.String</span></span>

### <span data-ttu-id="9347c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9347c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="9347c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9347c-140">OUTPUTS</span></span>

### <span data-ttu-id="9347c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9347c-141">System.Boolean</span></span>

## <span data-ttu-id="9347c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9347c-142">NOTES</span></span>
* <span data-ttu-id="9347c-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="9347c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9347c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9347c-144">RELATED LINKS</span></span>

[<span data-ttu-id="9347c-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9347c-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="9347c-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9347c-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


