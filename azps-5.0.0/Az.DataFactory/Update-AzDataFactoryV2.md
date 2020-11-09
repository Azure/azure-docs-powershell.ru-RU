---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313673"
---
# <span data-ttu-id="716cf-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="716cf-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="716cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="716cf-102">SYNOPSIS</span></span>
<span data-ttu-id="716cf-103">Обновляет свойства фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="716cf-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="716cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="716cf-104">SYNTAX</span></span>

### <span data-ttu-id="716cf-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="716cf-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="716cf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="716cf-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="716cf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="716cf-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716cf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="716cf-108">DESCRIPTION</span></span>
<span data-ttu-id="716cf-109">Командлет **Update-AzDataFactoryV2** обновляет Теги и свойства идентификаторов фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="716cf-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="716cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="716cf-110">EXAMPLES</span></span>

### <span data-ttu-id="716cf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="716cf-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="716cf-112">Эта команда обновляет Теги фабрики WikiADF с помощью словаря, содержащего тег с именем myNewTagName и значением myTagValue.</span><span class="sxs-lookup"><span data-stu-id="716cf-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="716cf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="716cf-113">PARAMETERS</span></span>

### <span data-ttu-id="716cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716cf-114">-DefaultProfile</span></span>
<span data-ttu-id="716cf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="716cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="716cf-116">-InputObject</span></span>
<span data-ttu-id="716cf-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="716cf-117">The data factory object.</span></span>

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

### <span data-ttu-id="716cf-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="716cf-118">-Name</span></span>
<span data-ttu-id="716cf-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="716cf-119">The data factory name.</span></span>

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

### <span data-ttu-id="716cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="716cf-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="716cf-121">The resource group name.</span></span>

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

### <span data-ttu-id="716cf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="716cf-122">-ResourceId</span></span>
<span data-ttu-id="716cf-123">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="716cf-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="716cf-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="716cf-124">-Tag</span></span>
<span data-ttu-id="716cf-125">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="716cf-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="716cf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="716cf-126">-Confirm</span></span>
<span data-ttu-id="716cf-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="716cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716cf-128">-WhatIf</span></span>
<span data-ttu-id="716cf-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="716cf-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="716cf-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="716cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716cf-131">CommonParameters</span></span>
<span data-ttu-id="716cf-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="716cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716cf-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716cf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716cf-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="716cf-134">INPUTS</span></span>

### <span data-ttu-id="716cf-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="716cf-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="716cf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="716cf-136">System.String</span></span>

## <span data-ttu-id="716cf-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="716cf-137">OUTPUTS</span></span>

### <span data-ttu-id="716cf-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="716cf-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="716cf-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="716cf-139">NOTES</span></span>

## <span data-ttu-id="716cf-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="716cf-140">RELATED LINKS</span></span>
