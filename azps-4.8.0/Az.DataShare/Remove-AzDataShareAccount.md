---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077825"
---
# <span data-ttu-id="b17a1-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b17a1-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="b17a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b17a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b17a1-103">Удаление учетной записи "общий доступ к файлам"</span><span class="sxs-lookup"><span data-stu-id="b17a1-103">Removes a datashare account</span></span>

## <span data-ttu-id="b17a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b17a1-104">SYNTAX</span></span>

### <span data-ttu-id="b17a1-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b17a1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b17a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b17a1-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b17a1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b17a1-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b17a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b17a1-108">DESCRIPTION</span></span>
<span data-ttu-id="b17a1-109">Командлет **Remove-AzDataShareAccount** удаляет учетную запись "общий доступ к файлам".</span><span class="sxs-lookup"><span data-stu-id="b17a1-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="b17a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b17a1-110">EXAMPLES</span></span>

### <span data-ttu-id="b17a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b17a1-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b17a1-112">Эта команда удаляет учетную запись с именем WikiADS из группы ресурсов с именем ADS.</span><span class="sxs-lookup"><span data-stu-id="b17a1-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="b17a1-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="b17a1-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b17a1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b17a1-114">PARAMETERS</span></span>

### <span data-ttu-id="b17a1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b17a1-115">-AsJob</span></span>
<span data-ttu-id="b17a1-116">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="b17a1-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b17a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17a1-117">-DefaultProfile</span></span>
<span data-ttu-id="b17a1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b17a1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b17a1-119">-Force</span></span>
<span data-ttu-id="b17a1-120">{Определение принудительной заливки}}</span><span class="sxs-lookup"><span data-stu-id="b17a1-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="b17a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b17a1-121">-InputObject</span></span>
<span data-ttu-id="b17a1-122">Объект учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a1-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b17a1-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b17a1-123">-Name</span></span>
<span data-ttu-id="b17a1-124">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a1-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="b17a1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b17a1-125">-PassThru</span></span>
<span data-ttu-id="b17a1-126">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="b17a1-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="b17a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b17a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="b17a1-128">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a1-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="b17a1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b17a1-129">-ResourceId</span></span>
<span data-ttu-id="b17a1-130">Идентификатор ресурса учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a1-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="b17a1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b17a1-131">-Confirm</span></span>
<span data-ttu-id="b17a1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b17a1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b17a1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b17a1-133">-WhatIf</span></span>
<span data-ttu-id="b17a1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b17a1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b17a1-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b17a1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b17a1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17a1-136">CommonParameters</span></span>
<span data-ttu-id="b17a1-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b17a1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17a1-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b17a1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17a1-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b17a1-139">INPUTS</span></span>

### <span data-ttu-id="b17a1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b17a1-140">System.String</span></span>

### <span data-ttu-id="b17a1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b17a1-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="b17a1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b17a1-142">OUTPUTS</span></span>

### <span data-ttu-id="b17a1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b17a1-143">System.Boolean</span></span>

## <span data-ttu-id="b17a1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b17a1-144">NOTES</span></span>

## <span data-ttu-id="b17a1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b17a1-145">RELATED LINKS</span></span>
