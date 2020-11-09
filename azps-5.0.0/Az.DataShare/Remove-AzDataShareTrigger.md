---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312872"
---
# <span data-ttu-id="aa2e4-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="aa2e4-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="aa2e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2e4-103">Удаление триггера</span><span class="sxs-lookup"><span data-stu-id="aa2e4-103">removes a trigger</span></span>

## <span data-ttu-id="aa2e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa2e4-104">SYNTAX</span></span>

### <span data-ttu-id="aa2e4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa2e4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa2e4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa2e4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2e4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa2e4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa2e4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa2e4-108">DESCRIPTION</span></span>
<span data-ttu-id="aa2e4-109">Командлет **Remove-AzDataShareTrigger** удаляет триггер общего доступа к файлам</span><span class="sxs-lookup"><span data-stu-id="aa2e4-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="aa2e4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa2e4-110">EXAMPLES</span></span>

### <span data-ttu-id="aa2e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa2e4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="aa2e4-112">Эти команды удаляют триггер с именем AdsTrigger из раздела Общий доступ к AdsShareSubscriptionу подписки.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="aa2e4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa2e4-113">PARAMETERS</span></span>

### <span data-ttu-id="aa2e4-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="aa2e4-114">-AccountName</span></span>
<span data-ttu-id="aa2e4-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa2e4-116">-AsJob</span></span>
<span data-ttu-id="aa2e4-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="aa2e4-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="aa2e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2e4-118">-DefaultProfile</span></span>
<span data-ttu-id="aa2e4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2e4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2e4-120">-InputObject</span></span>
<span data-ttu-id="aa2e4-121">Объект триггера общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa2e4-122">-Name</span></span>
<span data-ttu-id="aa2e4-123">Имя триггера общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-123">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa2e4-124">-PassThru</span></span>
<span data-ttu-id="aa2e4-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="aa2e4-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="aa2e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa2e4-127">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2e4-128">-ResourceId</span></span>
<span data-ttu-id="aa2e4-129">Идентификатор ресурса триггера общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-129">The resource id of azure data share trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="aa2e4-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="aa2e4-131">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="aa2e4-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2e4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa2e4-132">-Confirm</span></span>
<span data-ttu-id="aa2e4-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2e4-134">-WhatIf</span></span>
<span data-ttu-id="aa2e4-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa2e4-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa2e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2e4-137">CommonParameters</span></span>
<span data-ttu-id="aa2e4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa2e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2e4-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa2e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2e4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa2e4-140">INPUTS</span></span>

### <span data-ttu-id="aa2e4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aa2e4-141">System.String</span></span>

### <span data-ttu-id="aa2e4-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="aa2e4-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="aa2e4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa2e4-143">OUTPUTS</span></span>

### <span data-ttu-id="aa2e4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa2e4-144">System.Boolean</span></span>

## <span data-ttu-id="aa2e4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa2e4-145">NOTES</span></span>

## <span data-ttu-id="aa2e4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa2e4-146">RELATED LINKS</span></span>