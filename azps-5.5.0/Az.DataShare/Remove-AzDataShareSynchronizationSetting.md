---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228625"
---
# <span data-ttu-id="18fa3-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="18fa3-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="18fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="18fa3-103">удаление параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="18fa3-103">removes a synchronization setting</span></span>

## <span data-ttu-id="18fa3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18fa3-104">SYNTAX</span></span>

### <span data-ttu-id="18fa3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18fa3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18fa3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18fa3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18fa3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18fa3-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18fa3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="18fa3-109">При **настройке Remove-AzDataShareSynchronizationSetting параметр** синхронизации datashare удаляется.</span><span class="sxs-lookup"><span data-stu-id="18fa3-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="18fa3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18fa3-110">EXAMPLES</span></span>

### <span data-ttu-id="18fa3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18fa3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="18fa3-112">Эти команды удаляют параметр синхронизации AdsShareSynchronizationSetting из share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="18fa3-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="18fa3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18fa3-113">PARAMETERS</span></span>

### <span data-ttu-id="18fa3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18fa3-114">-AccountName</span></span>
<span data-ttu-id="18fa3-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="18fa3-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="18fa3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18fa3-116">-AsJob</span></span>
<span data-ttu-id="18fa3-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="18fa3-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="18fa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fa3-118">-DefaultProfile</span></span>
<span data-ttu-id="18fa3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18fa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18fa3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18fa3-120">-InputObject</span></span>
<span data-ttu-id="18fa3-121">Параметр синхронизации службы обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="18fa3-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18fa3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="18fa3-122">-Name</span></span>
<span data-ttu-id="18fa3-123">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="18fa3-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="18fa3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18fa3-124">-PassThru</span></span>
<span data-ttu-id="18fa3-125">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="18fa3-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="18fa3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fa3-126">-ResourceGroupName</span></span>
<span data-ttu-id="18fa3-127">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="18fa3-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="18fa3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18fa3-128">-ResourceId</span></span>
<span data-ttu-id="18fa3-129">ИД ресурса параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="18fa3-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="18fa3-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="18fa3-130">-ShareName</span></span>
<span data-ttu-id="18fa3-131">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="18fa3-131">Azure data share name</span></span>

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

### <span data-ttu-id="18fa3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18fa3-132">-Confirm</span></span>
<span data-ttu-id="18fa3-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fa3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18fa3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18fa3-134">-WhatIf</span></span>
<span data-ttu-id="18fa3-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fa3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18fa3-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18fa3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18fa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fa3-137">CommonParameters</span></span>
<span data-ttu-id="18fa3-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fa3-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18fa3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fa3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18fa3-140">INPUTS</span></span>

### <span data-ttu-id="18fa3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="18fa3-141">System.String</span></span>

### <span data-ttu-id="18fa3-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="18fa3-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="18fa3-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18fa3-143">OUTPUTS</span></span>

### <span data-ttu-id="18fa3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18fa3-144">System.Boolean</span></span>

## <span data-ttu-id="18fa3-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18fa3-145">NOTES</span></span>

## <span data-ttu-id="18fa3-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18fa3-146">RELATED LINKS</span></span>
