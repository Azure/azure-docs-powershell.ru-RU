---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: a2bcfa4232c7e69bdb17a5d56ff7b79373593b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721156"
---
# <span data-ttu-id="6d5b5-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6d5b5-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="6d5b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5b5-103">Удаление подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-103">removes a share subscription</span></span>

## <span data-ttu-id="6d5b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d5b5-104">SYNTAX</span></span>

### <span data-ttu-id="6d5b5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d5b5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d5b5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d5b5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d5b5-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d5b5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-108">DESCRIPTION</span></span>
<span data-ttu-id="6d5b5-109">Командлет **Remove-AzDataShareSubscription** удаляет подписку на общий доступ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="6d5b5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-110">EXAMPLES</span></span>

### <span data-ttu-id="6d5b5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d5b5-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6d5b5-112">Эти команды удаляют sharesubscription с именем AdsShareSubscription из учетной записи WikiAds.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="6d5b5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-113">PARAMETERS</span></span>

### <span data-ttu-id="6d5b5-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6d5b5-114">-AccountName</span></span>
<span data-ttu-id="6d5b5-115">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="6d5b5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d5b5-116">-AsJob</span></span>
<span data-ttu-id="6d5b5-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="6d5b5-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="6d5b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5b5-118">-DefaultProfile</span></span>
<span data-ttu-id="6d5b5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5b5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5b5-120">-InputObject</span></span>
<span data-ttu-id="6d5b5-121">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="6d5b5-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5b5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-122">-Name</span></span>
<span data-ttu-id="6d5b5-123">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="6d5b5-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6d5b5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d5b5-124">-PassThru</span></span>
<span data-ttu-id="6d5b5-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="6d5b5-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="6d5b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d5b5-127">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="6d5b5-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6d5b5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d5b5-128">-ResourceId</span></span>
<span data-ttu-id="6d5b5-129">Идентификатор ресурса для подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="6d5b5-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="6d5b5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d5b5-130">-Confirm</span></span>
<span data-ttu-id="6d5b5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5b5-132">-WhatIf</span></span>
<span data-ttu-id="6d5b5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5b5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5b5-135">CommonParameters</span></span>
<span data-ttu-id="6d5b5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5b5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5b5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5b5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d5b5-138">INPUTS</span></span>

### <span data-ttu-id="6d5b5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6d5b5-139">System.String</span></span>

### <span data-ttu-id="6d5b5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6d5b5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="6d5b5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-141">OUTPUTS</span></span>

### <span data-ttu-id="6d5b5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d5b5-142">System.Boolean</span></span>

## <span data-ttu-id="6d5b5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d5b5-143">NOTES</span></span>

## <span data-ttu-id="6d5b5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d5b5-144">RELATED LINKS</span></span>
