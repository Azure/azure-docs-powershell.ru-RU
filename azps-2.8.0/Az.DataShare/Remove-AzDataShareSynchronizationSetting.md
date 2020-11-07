---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 0ff167f14c9a831cb2afe2ce335a0c8bcd18acc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721155"
---
# <span data-ttu-id="9579d-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9579d-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9579d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9579d-102">SYNOPSIS</span></span>
<span data-ttu-id="9579d-103">Удаление параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="9579d-103">removes a synchronization setting</span></span>

## <span data-ttu-id="9579d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9579d-104">SYNTAX</span></span>

### <span data-ttu-id="9579d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9579d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9579d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9579d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9579d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9579d-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9579d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9579d-108">DESCRIPTION</span></span>
<span data-ttu-id="9579d-109">Командлет **Remove-AzDataShareSynchronizationSetting** удаляет параметр синхронизации для общего доступа к файлам</span><span class="sxs-lookup"><span data-stu-id="9579d-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="9579d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9579d-110">EXAMPLES</span></span>

### <span data-ttu-id="9579d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9579d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="9579d-112">Эти команды удаляют параметр синхронизации с именем AdsShareSynchronizationSetting из общего доступа AdsShare.</span><span class="sxs-lookup"><span data-stu-id="9579d-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="9579d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9579d-113">PARAMETERS</span></span>

### <span data-ttu-id="9579d-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9579d-114">-AccountName</span></span>
<span data-ttu-id="9579d-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9579d-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="9579d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9579d-116">-AsJob</span></span>
<span data-ttu-id="9579d-117">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="9579d-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9579d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9579d-118">-DefaultProfile</span></span>
<span data-ttu-id="9579d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9579d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9579d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9579d-120">-InputObject</span></span>
<span data-ttu-id="9579d-121">Параметр синхронизации общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="9579d-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="9579d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9579d-122">-Name</span></span>
<span data-ttu-id="9579d-123">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="9579d-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="9579d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9579d-124">-PassThru</span></span>
<span data-ttu-id="9579d-125">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="9579d-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9579d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9579d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9579d-127">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9579d-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9579d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9579d-128">-ResourceId</span></span>
<span data-ttu-id="9579d-129">Идентификатор ресурса параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="9579d-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="9579d-130">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="9579d-130">-ShareName</span></span>
<span data-ttu-id="9579d-131">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9579d-131">Azure data share name</span></span>

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

### <span data-ttu-id="9579d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9579d-132">-Confirm</span></span>
<span data-ttu-id="9579d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9579d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9579d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9579d-134">-WhatIf</span></span>
<span data-ttu-id="9579d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9579d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9579d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9579d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9579d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9579d-137">CommonParameters</span></span>
<span data-ttu-id="9579d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9579d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9579d-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9579d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9579d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9579d-140">INPUTS</span></span>

### <span data-ttu-id="9579d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9579d-141">System.String</span></span>

### <span data-ttu-id="9579d-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9579d-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9579d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9579d-143">OUTPUTS</span></span>

### <span data-ttu-id="9579d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9579d-144">System.Boolean</span></span>

## <span data-ttu-id="9579d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9579d-145">NOTES</span></span>

## <span data-ttu-id="9579d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9579d-146">RELATED LINKS</span></span>
