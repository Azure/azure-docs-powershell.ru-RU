---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236376"
---
# <span data-ttu-id="27ebf-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="27ebf-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="27ebf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="27ebf-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="27ebf-103">Removes a data factory.</span></span>

## <span data-ttu-id="27ebf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ebf-104">SYNTAX</span></span>

### <span data-ttu-id="27ebf-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27ebf-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ebf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="27ebf-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ebf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ebf-107">DESCRIPTION</span></span>
<span data-ttu-id="27ebf-108">Командлет **Remove-AzDataFactory** удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="27ebf-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="27ebf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ebf-109">EXAMPLES</span></span>

### <span data-ttu-id="27ebf-110">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="27ebf-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="27ebf-111">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="27ebf-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="27ebf-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="27ebf-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="27ebf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="27ebf-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="27ebf-114">-DataFactory</span></span>
<span data-ttu-id="27ebf-115">Указывает объект **PSDataFactory** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="27ebf-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="27ebf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ebf-116">-DefaultProfile</span></span>
<span data-ttu-id="27ebf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="27ebf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27ebf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="27ebf-118">-Force</span></span>
<span data-ttu-id="27ebf-119">Указывает на то, что этот командлет удаляет фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="27ebf-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="27ebf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27ebf-120">-Name</span></span>
<span data-ttu-id="27ebf-121">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="27ebf-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ebf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ebf-122">-ResourceGroupName</span></span>
<span data-ttu-id="27ebf-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="27ebf-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="27ebf-124">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="27ebf-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="27ebf-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27ebf-125">-Confirm</span></span>
<span data-ttu-id="27ebf-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27ebf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ebf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ebf-127">-WhatIf</span></span>
<span data-ttu-id="27ebf-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27ebf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ebf-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27ebf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ebf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ebf-130">CommonParameters</span></span>
<span data-ttu-id="27ebf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ebf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ebf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ebf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ebf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ebf-133">INPUTS</span></span>

### <span data-ttu-id="27ebf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="27ebf-134">System.String</span></span>

### <span data-ttu-id="27ebf-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="27ebf-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="27ebf-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ebf-136">OUTPUTS</span></span>

### <span data-ttu-id="27ebf-137">System. void</span><span class="sxs-lookup"><span data-stu-id="27ebf-137">System.Void</span></span>

## <span data-ttu-id="27ebf-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ebf-138">NOTES</span></span>
* <span data-ttu-id="27ebf-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="27ebf-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="27ebf-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ebf-140">RELATED LINKS</span></span>

[<span data-ttu-id="27ebf-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="27ebf-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="27ebf-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="27ebf-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

