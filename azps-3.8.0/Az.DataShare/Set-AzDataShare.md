---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: c92348e32247bfed0b3aa7ce59b4772f7d3ef4af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074417"
---
# <span data-ttu-id="dce68-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="dce68-101">Set-AzDataShare</span></span>

## <span data-ttu-id="dce68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dce68-102">SYNOPSIS</span></span>
<span data-ttu-id="dce68-103">Обновление существующего общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="dce68-103">Updates an existing data share</span></span>

## <span data-ttu-id="dce68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dce68-104">SYNTAX</span></span>

### <span data-ttu-id="dce68-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dce68-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce68-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dce68-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce68-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dce68-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce68-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce68-108">DESCRIPTION</span></span>
<span data-ttu-id="dce68-109">Командлет **Set-AzDataShare** обновляет общий доступ к данным, который находится в указанной учетной записи для общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="dce68-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="dce68-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dce68-110">EXAMPLES</span></span>

### <span data-ttu-id="dce68-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dce68-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="dce68-112">Эта команда обновляет существующий общий доступ к данным с именем AdsShare</span><span class="sxs-lookup"><span data-stu-id="dce68-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="dce68-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dce68-113">PARAMETERS</span></span>

### <span data-ttu-id="dce68-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="dce68-114">-AccountName</span></span>
<span data-ttu-id="dce68-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="dce68-115">Azure data share account name</span></span>

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

### <span data-ttu-id="dce68-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce68-116">-DefaultProfile</span></span>
<span data-ttu-id="dce68-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dce68-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dce68-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="dce68-118">-Description</span></span>
<span data-ttu-id="dce68-119">Описание общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="dce68-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce68-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce68-120">-InputObject</span></span>
<span data-ttu-id="dce68-121">Объект общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="dce68-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce68-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dce68-122">-Name</span></span>
<span data-ttu-id="dce68-123">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="dce68-123">Azure data share name</span></span>

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

### <span data-ttu-id="dce68-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce68-124">-ResourceGroupName</span></span>
<span data-ttu-id="dce68-125">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="dce68-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="dce68-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dce68-126">-ResourceId</span></span>
<span data-ttu-id="dce68-127">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="dce68-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="dce68-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="dce68-128">-TermsOfUse</span></span>
<span data-ttu-id="dce68-129">Условия использования общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="dce68-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce68-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dce68-130">-Confirm</span></span>
<span data-ttu-id="dce68-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dce68-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce68-132">-WhatIf</span></span>
<span data-ttu-id="dce68-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dce68-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dce68-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dce68-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce68-135">CommonParameters</span></span>
<span data-ttu-id="dce68-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dce68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce68-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce68-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce68-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dce68-138">INPUTS</span></span>

### <span data-ttu-id="dce68-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dce68-139">System.String</span></span>

### <span data-ttu-id="dce68-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="dce68-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="dce68-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dce68-141">OUTPUTS</span></span>

### <span data-ttu-id="dce68-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="dce68-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="dce68-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dce68-143">NOTES</span></span>

## <span data-ttu-id="dce68-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dce68-144">RELATED LINKS</span></span>
