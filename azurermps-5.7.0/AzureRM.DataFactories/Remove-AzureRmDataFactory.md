---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561871"
---
# <span data-ttu-id="3a482-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a482-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="3a482-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a482-102">SYNOPSIS</span></span>
<span data-ttu-id="3a482-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3a482-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a482-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a482-104">SYNTAX</span></span>

### <span data-ttu-id="3a482-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a482-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a482-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3a482-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a482-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a482-107">DESCRIPTION</span></span>
<span data-ttu-id="3a482-108">Командлет **Remove-AzureRmDataFactory** удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="3a482-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="3a482-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a482-109">EXAMPLES</span></span>

### <span data-ttu-id="3a482-110">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="3a482-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="3a482-111">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="3a482-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="3a482-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3a482-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="3a482-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a482-113">PARAMETERS</span></span>

### <span data-ttu-id="3a482-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="3a482-114">-DataFactory</span></span>
<span data-ttu-id="3a482-115">Указывает объект **PSDataFactory** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3a482-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="3a482-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a482-116">-DefaultProfile</span></span>
<span data-ttu-id="3a482-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a482-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a482-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3a482-118">-Force</span></span>
<span data-ttu-id="3a482-119">Указывает на то, что этот командлет удаляет фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3a482-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3a482-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a482-120">-Name</span></span>
<span data-ttu-id="3a482-121">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3a482-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a482-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a482-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a482-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3a482-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3a482-124">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a482-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a482-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a482-125">-Confirm</span></span>
<span data-ttu-id="3a482-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a482-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a482-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a482-127">-WhatIf</span></span>
<span data-ttu-id="3a482-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a482-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a482-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a482-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a482-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a482-130">CommonParameters</span></span>
<span data-ttu-id="3a482-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a482-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a482-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a482-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a482-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a482-133">INPUTS</span></span>

### <span data-ttu-id="3a482-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="3a482-134">None</span></span>
<span data-ttu-id="3a482-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3a482-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a482-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a482-136">OUTPUTS</span></span>

### <span data-ttu-id="3a482-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a482-137">System.Boolean</span></span>

## <span data-ttu-id="3a482-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a482-138">NOTES</span></span>
* <span data-ttu-id="3a482-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3a482-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3a482-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a482-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a482-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a482-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="3a482-142">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a482-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


