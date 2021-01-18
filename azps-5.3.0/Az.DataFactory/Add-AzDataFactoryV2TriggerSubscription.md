---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519033"
---
# <span data-ttu-id="babc2-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="babc2-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="babc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="babc2-102">SYNOPSIS</span></span>
<span data-ttu-id="babc2-103">Подпишитесь на триггер события внешней службы.</span><span class="sxs-lookup"><span data-stu-id="babc2-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="babc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="babc2-104">SYNTAX</span></span>

### <span data-ttu-id="babc2-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="babc2-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="babc2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="babc2-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="babc2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="babc2-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="babc2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="babc2-108">DESCRIPTION</span></span>
<span data-ttu-id="babc2-109">Эта команда подписывает триггер события события на указанные события внешней службы из триггера.</span><span class="sxs-lookup"><span data-stu-id="babc2-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="babc2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="babc2-110">EXAMPLES</span></span>

### <span data-ttu-id="babc2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="babc2-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="babc2-112">Эта команда подпишет триггер BlobEnetTrigger1 на указанные события из ветвях триггера.</span><span class="sxs-lookup"><span data-stu-id="babc2-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="babc2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="babc2-113">PARAMETERS</span></span>

### <span data-ttu-id="babc2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="babc2-114">-DataFactoryName</span></span>
<span data-ttu-id="babc2-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="babc2-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="babc2-116">-DefaultProfile</span></span>
<span data-ttu-id="babc2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="babc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="babc2-118">-InputObject</span></span>
<span data-ttu-id="babc2-119">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="babc2-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="babc2-120">-Name</span></span>
<span data-ttu-id="babc2-121">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="babc2-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="babc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="babc2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="babc2-123">The resource group name.</span></span>

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

### <span data-ttu-id="babc2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="babc2-124">-ResourceId</span></span>
<span data-ttu-id="babc2-125">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="babc2-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="babc2-126">-Confirm</span></span>
<span data-ttu-id="babc2-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="babc2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="babc2-128">-WhatIf</span></span>
<span data-ttu-id="babc2-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="babc2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="babc2-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="babc2-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babc2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="babc2-131">CommonParameters</span></span>
<span data-ttu-id="babc2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="babc2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="babc2-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="babc2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="babc2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="babc2-134">INPUTS</span></span>

### <span data-ttu-id="babc2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="babc2-135">System.String</span></span>
<span data-ttu-id="babc2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="babc2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="babc2-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="babc2-137">OUTPUTS</span></span>

### <span data-ttu-id="babc2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="babc2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="babc2-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="babc2-139">NOTES</span></span>

## <span data-ttu-id="babc2-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="babc2-140">RELATED LINKS</span></span>

