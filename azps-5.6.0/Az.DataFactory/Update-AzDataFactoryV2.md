---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: c80716e53b6f3aec6c9196baebbcd333aed1582c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964824"
---
# <span data-ttu-id="b4c63-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b4c63-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="b4c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4c63-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c63-103">Обновляет свойства фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b4c63-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="b4c63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4c63-104">SYNTAX</span></span>

### <span data-ttu-id="b4c63-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4c63-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4c63-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b4c63-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4c63-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c63-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c63-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4c63-108">DESCRIPTION</span></span>
<span data-ttu-id="b4c63-109">Командлет **Update-AzDataFactoryV2** обновляет теги или свойства удостоверений фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b4c63-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="b4c63-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4c63-110">EXAMPLES</span></span>

### <span data-ttu-id="b4c63-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4c63-111">Example 1</span></span>
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

<span data-ttu-id="b4c63-112">Эта команда обновляет теги в фабрике WikiADF до словаря, содержащего тег myNewTagName со значением myTagValue.</span><span class="sxs-lookup"><span data-stu-id="b4c63-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="b4c63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4c63-113">PARAMETERS</span></span>

### <span data-ttu-id="b4c63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c63-114">-DefaultProfile</span></span>
<span data-ttu-id="b4c63-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4c63-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4c63-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4c63-116">-InputObject</span></span>
<span data-ttu-id="b4c63-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b4c63-117">The data factory object.</span></span>

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

### <span data-ttu-id="b4c63-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b4c63-118">-Name</span></span>
<span data-ttu-id="b4c63-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b4c63-119">The data factory name.</span></span>

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

### <span data-ttu-id="b4c63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c63-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4c63-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4c63-121">The resource group name.</span></span>

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

### <span data-ttu-id="b4c63-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c63-122">-ResourceId</span></span>
<span data-ttu-id="b4c63-123">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="b4c63-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4c63-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4c63-124">-Tag</span></span>
<span data-ttu-id="b4c63-125">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b4c63-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="b4c63-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4c63-126">-Confirm</span></span>
<span data-ttu-id="b4c63-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4c63-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c63-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c63-128">-WhatIf</span></span>
<span data-ttu-id="b4c63-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4c63-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4c63-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4c63-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c63-131">CommonParameters</span></span>
<span data-ttu-id="b4c63-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4c63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c63-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4c63-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c63-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4c63-134">INPUTS</span></span>

### <span data-ttu-id="b4c63-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b4c63-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="b4c63-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b4c63-136">System.String</span></span>

## <span data-ttu-id="b4c63-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4c63-137">OUTPUTS</span></span>

### <span data-ttu-id="b4c63-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b4c63-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b4c63-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4c63-139">NOTES</span></span>

## <span data-ttu-id="b4c63-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4c63-140">RELATED LINKS</span></span>
