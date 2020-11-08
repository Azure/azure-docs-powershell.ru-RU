---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072866"
---
# <span data-ttu-id="cbaae-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="cbaae-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="cbaae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbaae-102">SYNOPSIS</span></span>
<span data-ttu-id="cbaae-103">Удаление подписки на общий доступ</span><span class="sxs-lookup"><span data-stu-id="cbaae-103">removes a share subscription</span></span>

## <span data-ttu-id="cbaae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbaae-104">SYNTAX</span></span>

### <span data-ttu-id="cbaae-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbaae-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbaae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbaae-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbaae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbaae-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbaae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbaae-108">DESCRIPTION</span></span>
<span data-ttu-id="cbaae-109">Командлет **Remove-AzDataShareSubscription** удаляет подписку на общий доступ</span><span class="sxs-lookup"><span data-stu-id="cbaae-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="cbaae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbaae-110">EXAMPLES</span></span>

### <span data-ttu-id="cbaae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbaae-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="cbaae-112">Эти команды удаляют sharesubscription с именем AdsShareSubscription из учетной записи WikiAds.</span><span class="sxs-lookup"><span data-stu-id="cbaae-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="cbaae-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbaae-113">PARAMETERS</span></span>

### <span data-ttu-id="cbaae-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="cbaae-114">-AccountName</span></span>
<span data-ttu-id="cbaae-115">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="cbaae-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="cbaae-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbaae-116">-AsJob</span></span>
<span data-ttu-id="cbaae-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="cbaae-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="cbaae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbaae-118">-DefaultProfile</span></span>
<span data-ttu-id="cbaae-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbaae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbaae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbaae-120">-InputObject</span></span>
<span data-ttu-id="cbaae-121">Объект подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="cbaae-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="cbaae-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbaae-122">-Name</span></span>
<span data-ttu-id="cbaae-123">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="cbaae-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="cbaae-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbaae-124">-PassThru</span></span>
<span data-ttu-id="cbaae-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="cbaae-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="cbaae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbaae-126">-ResourceGroupName</span></span>
<span data-ttu-id="cbaae-127">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="cbaae-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cbaae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbaae-128">-ResourceId</span></span>
<span data-ttu-id="cbaae-129">Идентификатор ресурса для подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="cbaae-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="cbaae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbaae-130">-Confirm</span></span>
<span data-ttu-id="cbaae-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbaae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbaae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbaae-132">-WhatIf</span></span>
<span data-ttu-id="cbaae-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbaae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbaae-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbaae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbaae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbaae-135">CommonParameters</span></span>
<span data-ttu-id="cbaae-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbaae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbaae-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbaae-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbaae-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbaae-138">INPUTS</span></span>

### <span data-ttu-id="cbaae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cbaae-139">System.String</span></span>

### <span data-ttu-id="cbaae-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="cbaae-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="cbaae-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbaae-141">OUTPUTS</span></span>

### <span data-ttu-id="cbaae-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbaae-142">System.Boolean</span></span>

## <span data-ttu-id="cbaae-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbaae-143">NOTES</span></span>

## <span data-ttu-id="cbaae-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbaae-144">RELATED LINKS</span></span>
