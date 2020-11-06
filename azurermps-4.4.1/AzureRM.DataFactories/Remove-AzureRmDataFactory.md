---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 59f1eabbadda682c87917f41d96959c691b9e593
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567661"
---
# <span data-ttu-id="420ef-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="420ef-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="420ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="420ef-102">SYNOPSIS</span></span>
<span data-ttu-id="420ef-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="420ef-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="420ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="420ef-104">SYNTAX</span></span>

### <span data-ttu-id="420ef-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="420ef-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420ef-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="420ef-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="420ef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="420ef-107">DESCRIPTION</span></span>
<span data-ttu-id="420ef-108">Командлет **Remove-AzureRmDataFactory** удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="420ef-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="420ef-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="420ef-109">EXAMPLES</span></span>

### <span data-ttu-id="420ef-110">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="420ef-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="420ef-111">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="420ef-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="420ef-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="420ef-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="420ef-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="420ef-113">PARAMETERS</span></span>

### <span data-ttu-id="420ef-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="420ef-114">-DataFactory</span></span>
<span data-ttu-id="420ef-115">Указывает объект **PSDataFactory** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="420ef-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="420ef-116">-Force</span><span class="sxs-lookup"><span data-stu-id="420ef-116">-Force</span></span>
<span data-ttu-id="420ef-117">Указывает на то, что этот командлет удаляет фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="420ef-117">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="420ef-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="420ef-118">-Name</span></span>
<span data-ttu-id="420ef-119">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="420ef-119">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="420ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="420ef-121">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="420ef-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="420ef-122">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="420ef-122">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="420ef-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="420ef-123">-Confirm</span></span>
<span data-ttu-id="420ef-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="420ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420ef-125">-WhatIf</span></span>
<span data-ttu-id="420ef-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="420ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="420ef-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="420ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420ef-128">-DefaultProfile</span></span>
<span data-ttu-id="420ef-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="420ef-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="420ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420ef-130">CommonParameters</span></span>
<span data-ttu-id="420ef-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="420ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420ef-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420ef-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="420ef-133">INPUTS</span></span>

## <span data-ttu-id="420ef-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="420ef-134">OUTPUTS</span></span>

### <span data-ttu-id="420ef-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="420ef-135">System.Boolean</span></span>

## <span data-ttu-id="420ef-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="420ef-136">NOTES</span></span>
* <span data-ttu-id="420ef-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="420ef-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="420ef-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="420ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="420ef-139">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="420ef-139">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="420ef-140">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="420ef-140">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


