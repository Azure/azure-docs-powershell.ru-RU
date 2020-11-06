---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564583"
---
# <span data-ttu-id="4281d-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4281d-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4281d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4281d-102">SYNOPSIS</span></span>
<span data-ttu-id="4281d-103">Обновляет свойства фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4281d-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4281d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4281d-104">SYNTAX</span></span>

### <span data-ttu-id="4281d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4281d-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4281d-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4281d-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4281d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4281d-108">DESCRIPTION</span></span>
<span data-ttu-id="4281d-109">Командлет **Update-AzureRmDataFactoryV2** обновляет Теги и свойства идентификаторов фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4281d-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="4281d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4281d-110">EXAMPLES</span></span>

### <span data-ttu-id="4281d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4281d-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="4281d-112">Эта команда обновляет Теги фабрики WikiADF с помощью словаря, содержащего тег с именем myNewTagName и значением myTagValue.</span><span class="sxs-lookup"><span data-stu-id="4281d-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="4281d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4281d-113">PARAMETERS</span></span>

### <span data-ttu-id="4281d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4281d-114">-DefaultProfile</span></span>
<span data-ttu-id="4281d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4281d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4281d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4281d-116">-InputObject</span></span>
<span data-ttu-id="4281d-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4281d-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4281d-118">-Name</span></span>
<span data-ttu-id="4281d-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4281d-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4281d-120">-ResourceGroupName</span></span>
<span data-ttu-id="4281d-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4281d-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4281d-122">-ResourceId</span></span>
<span data-ttu-id="4281d-123">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="4281d-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="4281d-124">-Tag</span></span>
<span data-ttu-id="4281d-125">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4281d-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4281d-126">-Confirm</span></span>
<span data-ttu-id="4281d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4281d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4281d-128">-WhatIf</span></span>
<span data-ttu-id="4281d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4281d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4281d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4281d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4281d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4281d-131">CommonParameters</span></span>
<span data-ttu-id="4281d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4281d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4281d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4281d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4281d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4281d-134">INPUTS</span></span>

### <span data-ttu-id="4281d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4281d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="4281d-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4281d-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4281d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4281d-137">System.String</span></span>

## <span data-ttu-id="4281d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4281d-138">OUTPUTS</span></span>

### <span data-ttu-id="4281d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4281d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4281d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4281d-140">NOTES</span></span>

## <span data-ttu-id="4281d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4281d-141">RELATED LINKS</span></span>
