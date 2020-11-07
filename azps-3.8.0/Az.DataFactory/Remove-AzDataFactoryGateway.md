---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912823"
---
# <span data-ttu-id="79608-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79608-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="79608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79608-102">SYNOPSIS</span></span>
<span data-ttu-id="79608-103">Удаляет шлюз из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="79608-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="79608-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79608-104">SYNTAX</span></span>

### <span data-ttu-id="79608-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79608-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79608-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="79608-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79608-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79608-107">DESCRIPTION</span></span>
<span data-ttu-id="79608-108">Командлет **Remove-AzDataFactoryGateway** удаляет указанный шлюз из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="79608-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="79608-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79608-109">EXAMPLES</span></span>

### <span data-ttu-id="79608-110">Пример 1: Удаление шлюза</span><span class="sxs-lookup"><span data-stu-id="79608-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="79608-111">Эта команда удаляет шлюз с именем ContosoGateway из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="79608-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="79608-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79608-112">PARAMETERS</span></span>

### <span data-ttu-id="79608-113">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="79608-113">-DataFactory</span></span>
<span data-ttu-id="79608-114">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="79608-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="79608-115">Этот командлет удаляет шлюз из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="79608-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79608-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79608-116">-DataFactoryName</span></span>
<span data-ttu-id="79608-117">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="79608-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="79608-118">Этот командлет удаляет шлюз из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="79608-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79608-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79608-119">-DefaultProfile</span></span>
<span data-ttu-id="79608-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="79608-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79608-121">-Force</span><span class="sxs-lookup"><span data-stu-id="79608-121">-Force</span></span>
<span data-ttu-id="79608-122">Указывает на то, что этот командлет удаляет шлюз без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="79608-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="79608-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79608-123">-Name</span></span>
<span data-ttu-id="79608-124">Указывает имя шлюза, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="79608-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="79608-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79608-125">-ResourceGroupName</span></span>
<span data-ttu-id="79608-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="79608-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="79608-127">Этот командлет удаляет шлюз, принадлежащий к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="79608-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="79608-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79608-128">-Confirm</span></span>
<span data-ttu-id="79608-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79608-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79608-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79608-130">-WhatIf</span></span>
<span data-ttu-id="79608-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79608-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79608-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79608-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79608-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79608-133">CommonParameters</span></span>
<span data-ttu-id="79608-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79608-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79608-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79608-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79608-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79608-136">INPUTS</span></span>

### <span data-ttu-id="79608-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="79608-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="79608-138">System. String</span><span class="sxs-lookup"><span data-stu-id="79608-138">System.String</span></span>

## <span data-ttu-id="79608-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79608-139">OUTPUTS</span></span>

### <span data-ttu-id="79608-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79608-140">System.Boolean</span></span>

## <span data-ttu-id="79608-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="79608-141">NOTES</span></span>
* <span data-ttu-id="79608-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="79608-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="79608-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79608-143">RELATED LINKS</span></span>

[<span data-ttu-id="79608-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79608-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="79608-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79608-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="79608-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="79608-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


