---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215097"
---
# <span data-ttu-id="01d9f-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="01d9f-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="01d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="01d9f-103">Удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="01d9f-103">Removes a data factory.</span></span>

## <span data-ttu-id="01d9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01d9f-104">SYNTAX</span></span>

### <span data-ttu-id="01d9f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01d9f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01d9f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="01d9f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d9f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="01d9f-108">Для **удаления фабрики данных удаляется cmdlet Remove-AzDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="01d9f-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="01d9f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="01d9f-110">Пример 1. Удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="01d9f-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="01d9f-111">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="01d9f-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="01d9f-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="01d9f-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="01d9f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d9f-113">PARAMETERS</span></span>

### <span data-ttu-id="01d9f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="01d9f-114">-DataFactory</span></span>
<span data-ttu-id="01d9f-115">Определяет объект **PSDataFactory,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="01d9f-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="01d9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d9f-116">-DefaultProfile</span></span>
<span data-ttu-id="01d9f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01d9f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01d9f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01d9f-118">-Force</span></span>
<span data-ttu-id="01d9f-119">Указывает на то, что этот cmdlet удаляет фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="01d9f-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="01d9f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01d9f-120">-Name</span></span>
<span data-ttu-id="01d9f-121">Название фабрики данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="01d9f-121">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="01d9f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d9f-122">-ResourceGroupName</span></span>
<span data-ttu-id="01d9f-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="01d9f-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="01d9f-124">Этот cmdlet удаляет фабрику данных из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="01d9f-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="01d9f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01d9f-125">-Confirm</span></span>
<span data-ttu-id="01d9f-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d9f-127">-WhatIf</span></span>
<span data-ttu-id="01d9f-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d9f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d9f-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="01d9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d9f-130">CommonParameters</span></span>
<span data-ttu-id="01d9f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d9f-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d9f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d9f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01d9f-133">INPUTS</span></span>

### <span data-ttu-id="01d9f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="01d9f-134">System.String</span></span>

### <span data-ttu-id="01d9f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="01d9f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="01d9f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01d9f-136">OUTPUTS</span></span>

### <span data-ttu-id="01d9f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="01d9f-137">System.Void</span></span>

## <span data-ttu-id="01d9f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01d9f-138">NOTES</span></span>
* <span data-ttu-id="01d9f-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="01d9f-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="01d9f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01d9f-140">RELATED LINKS</span></span>

[<span data-ttu-id="01d9f-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="01d9f-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="01d9f-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="01d9f-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


