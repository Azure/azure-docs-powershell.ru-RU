---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313805"
---
# <span data-ttu-id="0fbd2-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="0fbd2-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="0fbd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbd2-103">Отменяйте подписку триггера события на внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="0fbd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fbd2-104">SYNTAX</span></span>

### <span data-ttu-id="0fbd2-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fbd2-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fbd2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0fbd2-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fbd2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0fbd2-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fbd2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fbd2-108">DESCRIPTION</span></span>
<span data-ttu-id="0fbd2-109">Эта команда отменяет подписку триггера событий на указанные внешние события службы из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="0fbd2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fbd2-110">EXAMPLES</span></span>

### <span data-ttu-id="0fbd2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fbd2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="0fbd2-112">Эта команда позволяет отменить подписку на BlobEnetTrigger1 триггер для указанных событий из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="0fbd2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fbd2-113">PARAMETERS</span></span>

### <span data-ttu-id="0fbd2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0fbd2-114">-DataFactoryName</span></span>
<span data-ttu-id="0fbd2-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-115">The data factory name.</span></span>

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

### <span data-ttu-id="0fbd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbd2-116">-DefaultProfile</span></span>
<span data-ttu-id="0fbd2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbd2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0fbd2-118">-Force</span></span>
<span data-ttu-id="0fbd2-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0fbd2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fbd2-120">-InputObject</span></span>
<span data-ttu-id="0fbd2-121">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-121">The trigger object.</span></span>

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

### <span data-ttu-id="0fbd2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fbd2-122">-Name</span></span>
<span data-ttu-id="0fbd2-123">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-123">The trigger name.</span></span>

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

### <span data-ttu-id="0fbd2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fbd2-124">-PassThru</span></span>
<span data-ttu-id="0fbd2-125">Если задано, командлет вернет значение истина для успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="0fbd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="0fbd2-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-127">The resource group name.</span></span>

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

### <span data-ttu-id="0fbd2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fbd2-128">-ResourceId</span></span>
<span data-ttu-id="0fbd2-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0fbd2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fbd2-130">-Confirm</span></span>
<span data-ttu-id="0fbd2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbd2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbd2-132">-WhatIf</span></span>
<span data-ttu-id="0fbd2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fbd2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbd2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbd2-135">CommonParameters</span></span>
<span data-ttu-id="0fbd2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fbd2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbd2-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbd2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbd2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fbd2-138">INPUTS</span></span>

### <span data-ttu-id="0fbd2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0fbd2-139">System.String</span></span>
<span data-ttu-id="0fbd2-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0fbd2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0fbd2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fbd2-141">OUTPUTS</span></span>

### <span data-ttu-id="0fbd2-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0fbd2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="0fbd2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fbd2-143">NOTES</span></span>

## <span data-ttu-id="0fbd2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fbd2-144">RELATED LINKS</span></span>
