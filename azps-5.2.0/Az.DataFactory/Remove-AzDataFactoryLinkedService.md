---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417828"
---
# <span data-ttu-id="13336-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13336-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="13336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13336-102">SYNOPSIS</span></span>
<span data-ttu-id="13336-103">Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="13336-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="13336-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13336-104">SYNTAX</span></span>

### <span data-ttu-id="13336-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13336-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13336-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13336-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13336-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13336-107">DESCRIPTION</span></span>
<span data-ttu-id="13336-108">Для удаления связанной службы из фабрики данных Azure удаляется ее **cmdlet Remove-AzDataFactoryLinkedService.**</span><span class="sxs-lookup"><span data-stu-id="13336-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="13336-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13336-109">EXAMPLES</span></span>

### <span data-ttu-id="13336-110">Пример 1. Удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="13336-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="13336-111">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="13336-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="13336-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="13336-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="13336-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13336-113">PARAMETERS</span></span>

### <span data-ttu-id="13336-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="13336-114">-DataFactory</span></span>
<span data-ttu-id="13336-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="13336-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="13336-116">Этот cmdlet удаляет связанную службу из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="13336-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13336-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13336-117">-DataFactoryName</span></span>
<span data-ttu-id="13336-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="13336-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="13336-119">Этот cmdlet удаляет связанную службу из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="13336-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13336-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13336-120">-DefaultProfile</span></span>
<span data-ttu-id="13336-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="13336-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13336-122">-Force</span><span class="sxs-lookup"><span data-stu-id="13336-122">-Force</span></span>
<span data-ttu-id="13336-123">Указывает на то, что этот cmdlet удаляет связанную службу без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13336-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="13336-124">-Name</span><span class="sxs-lookup"><span data-stu-id="13336-124">-Name</span></span>
<span data-ttu-id="13336-125">Указывает имя связанной службы, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="13336-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13336-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13336-126">-ResourceGroupName</span></span>
<span data-ttu-id="13336-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="13336-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="13336-128">Этот cmdlet удаляет связанную службу из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="13336-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="13336-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13336-129">-Confirm</span></span>
<span data-ttu-id="13336-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13336-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13336-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13336-131">-WhatIf</span></span>
<span data-ttu-id="13336-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13336-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13336-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="13336-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13336-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13336-134">CommonParameters</span></span>
<span data-ttu-id="13336-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13336-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13336-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13336-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13336-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13336-137">INPUTS</span></span>

### <span data-ttu-id="13336-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13336-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="13336-139">System.String</span><span class="sxs-lookup"><span data-stu-id="13336-139">System.String</span></span>

## <span data-ttu-id="13336-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13336-140">OUTPUTS</span></span>

### <span data-ttu-id="13336-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="13336-141">System.Void</span></span>

## <span data-ttu-id="13336-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13336-142">NOTES</span></span>
* <span data-ttu-id="13336-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="13336-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13336-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13336-144">RELATED LINKS</span></span>

[<span data-ttu-id="13336-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13336-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="13336-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13336-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


