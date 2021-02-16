---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242776"
---
# <span data-ttu-id="0a1dd-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="0a1dd-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="0a1dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1dd-103">Отписать триггер событий для событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="0a1dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a1dd-104">SYNTAX</span></span>

### <span data-ttu-id="0a1dd-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a1dd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a1dd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a1dd-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1dd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a1dd-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a1dd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="0a1dd-109">Эта команда отписывает триггер события к указанным событиям внешней службы из триггера.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="0a1dd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a1dd-110">EXAMPLES</span></span>

### <span data-ttu-id="0a1dd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a1dd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="0a1dd-112">Эта команда отвязывает триггер BlobEnetTrigger1 к указанным событиям триггера.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="0a1dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a1dd-113">PARAMETERS</span></span>

### <span data-ttu-id="0a1dd-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0a1dd-114">-DataFactoryName</span></span>
<span data-ttu-id="0a1dd-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-115">The data factory name.</span></span>

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

### <span data-ttu-id="0a1dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1dd-116">-DefaultProfile</span></span>
<span data-ttu-id="0a1dd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a1dd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0a1dd-118">-Force</span></span>
<span data-ttu-id="0a1dd-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0a1dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a1dd-120">-InputObject</span></span>
<span data-ttu-id="0a1dd-121">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-121">The trigger object.</span></span>

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

### <span data-ttu-id="0a1dd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0a1dd-122">-Name</span></span>
<span data-ttu-id="0a1dd-123">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-123">The trigger name.</span></span>

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

### <span data-ttu-id="0a1dd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a1dd-124">-PassThru</span></span>
<span data-ttu-id="0a1dd-125">При этом возвращается "Истина" при успешном удалении.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="0a1dd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a1dd-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a1dd-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-127">The resource group name.</span></span>

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

### <span data-ttu-id="0a1dd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a1dd-128">-ResourceId</span></span>
<span data-ttu-id="0a1dd-129">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0a1dd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a1dd-130">-Confirm</span></span>
<span data-ttu-id="0a1dd-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a1dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1dd-132">-WhatIf</span></span>
<span data-ttu-id="0a1dd-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a1dd-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a1dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1dd-135">CommonParameters</span></span>
<span data-ttu-id="0a1dd-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1dd-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1dd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1dd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a1dd-138">INPUTS</span></span>

### <span data-ttu-id="0a1dd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0a1dd-139">System.String</span></span>
<span data-ttu-id="0a1dd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0a1dd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0a1dd-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a1dd-141">OUTPUTS</span></span>

### <span data-ttu-id="0a1dd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0a1dd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="0a1dd-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a1dd-143">NOTES</span></span>

## <span data-ttu-id="0a1dd-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a1dd-144">RELATED LINKS</span></span>

