---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077819"
---
# <span data-ttu-id="014da-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="014da-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="014da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="014da-102">SYNOPSIS</span></span>
<span data-ttu-id="014da-103">Удаление приглашения</span><span class="sxs-lookup"><span data-stu-id="014da-103">removes an invitation</span></span>

## <span data-ttu-id="014da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="014da-104">SYNTAX</span></span>

### <span data-ttu-id="014da-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="014da-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="014da-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="014da-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014da-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="014da-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014da-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="014da-108">DESCRIPTION</span></span>
<span data-ttu-id="014da-109">Командлет **Remove-AzDataShareInvitation** удаляет приглашение на доступ к файлам.</span><span class="sxs-lookup"><span data-stu-id="014da-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="014da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="014da-110">EXAMPLES</span></span>

### <span data-ttu-id="014da-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="014da-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="014da-112">Эта команда удаляет приглашение с именем ADSInvite из общего доступа AdsShare.</span><span class="sxs-lookup"><span data-stu-id="014da-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="014da-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="014da-113">PARAMETERS</span></span>

### <span data-ttu-id="014da-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="014da-114">-AccountName</span></span>
<span data-ttu-id="014da-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="014da-115">Azure data share account name</span></span>

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

### <span data-ttu-id="014da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014da-116">-DefaultProfile</span></span>
<span data-ttu-id="014da-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="014da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="014da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="014da-118">-InputObject</span></span>
<span data-ttu-id="014da-119">Объект приглашения на доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="014da-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="014da-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="014da-120">-Name</span></span>
<span data-ttu-id="014da-121">Имя приглашения на предоставление данных Azure</span><span class="sxs-lookup"><span data-stu-id="014da-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="014da-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="014da-122">-PassThru</span></span>
<span data-ttu-id="014da-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="014da-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="014da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014da-124">-ResourceGroupName</span></span>
<span data-ttu-id="014da-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="014da-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="014da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="014da-126">-ResourceId</span></span>
<span data-ttu-id="014da-127">Идентификатор ресурса для приглашения на доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="014da-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="014da-128">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="014da-128">-ShareName</span></span>
<span data-ttu-id="014da-129">Имя общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="014da-129">Azure data share name.</span></span>

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

### <span data-ttu-id="014da-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="014da-130">-Confirm</span></span>
<span data-ttu-id="014da-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="014da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014da-132">-WhatIf</span></span>
<span data-ttu-id="014da-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="014da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014da-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="014da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014da-135">CommonParameters</span></span>
<span data-ttu-id="014da-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="014da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014da-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="014da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014da-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="014da-138">INPUTS</span></span>

### <span data-ttu-id="014da-139">System. String</span><span class="sxs-lookup"><span data-stu-id="014da-139">System.String</span></span>

### <span data-ttu-id="014da-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="014da-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="014da-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="014da-141">OUTPUTS</span></span>

### <span data-ttu-id="014da-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="014da-142">System.Boolean</span></span>

## <span data-ttu-id="014da-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="014da-143">NOTES</span></span>

## <span data-ttu-id="014da-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="014da-144">RELATED LINKS</span></span>
