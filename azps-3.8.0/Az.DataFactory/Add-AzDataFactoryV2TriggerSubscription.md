---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074421"
---
# <span data-ttu-id="f6985-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="f6985-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="f6985-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6985-102">SYNOPSIS</span></span>
<span data-ttu-id="f6985-103">Подписка триггера события на внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="f6985-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="f6985-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6985-104">SYNTAX</span></span>

### <span data-ttu-id="f6985-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6985-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6985-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6985-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6985-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6985-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6985-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6985-108">DESCRIPTION</span></span>
<span data-ttu-id="f6985-109">Эта команда осуществляет подписку триггера событий на указанные внешние события службы из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="f6985-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="f6985-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6985-110">EXAMPLES</span></span>

### <span data-ttu-id="f6985-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6985-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="f6985-112">Эта команда будет подписаться на BlobEnetTrigger1 триггер к указанным событиям из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="f6985-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="f6985-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6985-113">PARAMETERS</span></span>

### <span data-ttu-id="f6985-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f6985-114">-DataFactoryName</span></span>
<span data-ttu-id="f6985-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f6985-115">The data factory name.</span></span>

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

### <span data-ttu-id="f6985-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6985-116">-DefaultProfile</span></span>
<span data-ttu-id="f6985-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6985-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6985-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6985-118">-InputObject</span></span>
<span data-ttu-id="f6985-119">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="f6985-119">The trigger object.</span></span>

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

### <span data-ttu-id="f6985-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6985-120">-Name</span></span>
<span data-ttu-id="f6985-121">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="f6985-121">The trigger name.</span></span>

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

### <span data-ttu-id="f6985-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6985-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6985-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6985-123">The resource group name.</span></span>

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

### <span data-ttu-id="f6985-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6985-124">-ResourceId</span></span>
<span data-ttu-id="f6985-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="f6985-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f6985-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6985-126">-Confirm</span></span>
<span data-ttu-id="f6985-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6985-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6985-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6985-128">-WhatIf</span></span>
<span data-ttu-id="f6985-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6985-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6985-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6985-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6985-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6985-131">CommonParameters</span></span>
<span data-ttu-id="f6985-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6985-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6985-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6985-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6985-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6985-134">INPUTS</span></span>

### <span data-ttu-id="f6985-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f6985-135">System.String</span></span>
<span data-ttu-id="f6985-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f6985-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f6985-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6985-137">OUTPUTS</span></span>

### <span data-ttu-id="f6985-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f6985-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f6985-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6985-139">NOTES</span></span>

## <span data-ttu-id="f6985-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6985-140">RELATED LINKS</span></span>

