---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 8144d1989f6bec9c1342613cf4776a6dae0a9c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972056"
---
# <span data-ttu-id="833ac-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="833ac-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="833ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="833ac-102">SYNOPSIS</span></span>
<span data-ttu-id="833ac-103">Удаляет концентратор из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="833ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="833ac-104">SYNTAX</span></span>

### <span data-ttu-id="833ac-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="833ac-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="833ac-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="833ac-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="833ac-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="833ac-107">DESCRIPTION</span></span>
<span data-ttu-id="833ac-108">Для удаления концентратора **из** фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных удаляется концентратор.</span><span class="sxs-lookup"><span data-stu-id="833ac-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="833ac-109">При удалении концентратора также удаляются все связанные службы и конвейеры.</span><span class="sxs-lookup"><span data-stu-id="833ac-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="833ac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="833ac-110">EXAMPLES</span></span>

### <span data-ttu-id="833ac-111">Пример 1. Удаление концентратора</span><span class="sxs-lookup"><span data-stu-id="833ac-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="833ac-112">Эта команда удаляет концентратор ContosoDataHub из группы ресурсов Azure ADFResourceGroup и фабрики данных ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="833ac-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="833ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="833ac-113">PARAMETERS</span></span>

### <span data-ttu-id="833ac-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="833ac-114">-DataFactory</span></span>
<span data-ttu-id="833ac-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="833ac-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="833ac-116">Этот cmdlet удаляет концентратор из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="833ac-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="833ac-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="833ac-117">-DataFactoryName</span></span>
<span data-ttu-id="833ac-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="833ac-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="833ac-119">Этот cmdlet удаляет концентратор из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="833ac-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="833ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833ac-120">-DefaultProfile</span></span>
<span data-ttu-id="833ac-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="833ac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="833ac-122">-Force</span><span class="sxs-lookup"><span data-stu-id="833ac-122">-Force</span></span>
<span data-ttu-id="833ac-123">Указывает на то, что этот cmdlet удаляет концентратор без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="833ac-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="833ac-124">-Name</span><span class="sxs-lookup"><span data-stu-id="833ac-124">-Name</span></span>
<span data-ttu-id="833ac-125">Указывает имя концентратора, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="833ac-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="833ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="833ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="833ac-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="833ac-128">Этот cmdlet удаляет концентратор из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="833ac-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="833ac-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="833ac-129">-Confirm</span></span>
<span data-ttu-id="833ac-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="833ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="833ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="833ac-131">-WhatIf</span></span>
<span data-ttu-id="833ac-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="833ac-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="833ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="833ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833ac-134">CommonParameters</span></span>
<span data-ttu-id="833ac-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="833ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833ac-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="833ac-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833ac-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="833ac-137">INPUTS</span></span>

### <span data-ttu-id="833ac-138">System.String</span><span class="sxs-lookup"><span data-stu-id="833ac-138">System.String</span></span>

### <span data-ttu-id="833ac-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="833ac-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="833ac-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="833ac-140">OUTPUTS</span></span>

### <span data-ttu-id="833ac-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="833ac-141">System.Boolean</span></span>

## <span data-ttu-id="833ac-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="833ac-142">NOTES</span></span>
* <span data-ttu-id="833ac-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="833ac-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="833ac-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="833ac-144">RELATED LINKS</span></span>

[<span data-ttu-id="833ac-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="833ac-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="833ac-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="833ac-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


