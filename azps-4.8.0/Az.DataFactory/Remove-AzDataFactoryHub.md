---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077879"
---
# <span data-ttu-id="303f9-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="303f9-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="303f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="303f9-102">SYNOPSIS</span></span>
<span data-ttu-id="303f9-103">Удаляет концентратор из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="303f9-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="303f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="303f9-104">SYNTAX</span></span>

### <span data-ttu-id="303f9-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="303f9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="303f9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="303f9-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="303f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="303f9-107">DESCRIPTION</span></span>
<span data-ttu-id="303f9-108">Командлет **Remove-AzDataFactoryHub** удаляет концентратор из фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="303f9-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="303f9-109">При удалении концентратора также удаляются все связанные службы и конвейеры в центре.</span><span class="sxs-lookup"><span data-stu-id="303f9-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="303f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="303f9-110">EXAMPLES</span></span>

### <span data-ttu-id="303f9-111">Пример 1: удаление концентратора</span><span class="sxs-lookup"><span data-stu-id="303f9-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="303f9-112">Эта команда удаляет концентратор с именем ContosoDataHub из группы ресурсов Azure с именем ADFResourceGroup и фабрики данных под названием ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="303f9-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="303f9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="303f9-113">PARAMETERS</span></span>

### <span data-ttu-id="303f9-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="303f9-114">-DataFactory</span></span>
<span data-ttu-id="303f9-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="303f9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="303f9-116">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="303f9-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="303f9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="303f9-117">-DataFactoryName</span></span>
<span data-ttu-id="303f9-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="303f9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="303f9-119">Этот командлет удаляет концентратор из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="303f9-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="303f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303f9-120">-DefaultProfile</span></span>
<span data-ttu-id="303f9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="303f9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303f9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="303f9-122">-Force</span></span>
<span data-ttu-id="303f9-123">Указывает на то, что этот командлет удаляет концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="303f9-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="303f9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="303f9-124">-Name</span></span>
<span data-ttu-id="303f9-125">Указывает имя удаляемого узла.</span><span class="sxs-lookup"><span data-stu-id="303f9-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="303f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="303f9-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="303f9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="303f9-128">Этот командлет удаляет концентратор из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="303f9-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="303f9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="303f9-129">-Confirm</span></span>
<span data-ttu-id="303f9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="303f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303f9-131">-WhatIf</span></span>
<span data-ttu-id="303f9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="303f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="303f9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="303f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303f9-134">CommonParameters</span></span>
<span data-ttu-id="303f9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="303f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303f9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="303f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303f9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="303f9-137">INPUTS</span></span>

### <span data-ttu-id="303f9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="303f9-138">System.String</span></span>

### <span data-ttu-id="303f9-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="303f9-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="303f9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="303f9-140">OUTPUTS</span></span>

### <span data-ttu-id="303f9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="303f9-141">System.Boolean</span></span>

## <span data-ttu-id="303f9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="303f9-142">NOTES</span></span>
* <span data-ttu-id="303f9-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="303f9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="303f9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="303f9-144">RELATED LINKS</span></span>

[<span data-ttu-id="303f9-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="303f9-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="303f9-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="303f9-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


