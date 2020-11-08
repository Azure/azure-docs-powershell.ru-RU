---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246190"
---
# <span data-ttu-id="ddca1-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ddca1-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="ddca1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddca1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddca1-103">Обновление параметров безопасности в центре безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="ddca1-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="ddca1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddca1-104">SYNTAX</span></span>

### <span data-ttu-id="ddca1-105">GeneralScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddca1-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca1-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="ddca1-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ddca1-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddca1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddca1-108">DESCRIPTION</span></span>
<span data-ttu-id="ddca1-109">Командлет Set-AzSecuritySetting обновляет определенный параметр безопасности в центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="ddca1-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="ddca1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddca1-110">EXAMPLES</span></span>

### <span data-ttu-id="ddca1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddca1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="ddca1-112">Обновляет параметр экспорта данных MCAS</span><span class="sxs-lookup"><span data-stu-id="ddca1-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="ddca1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddca1-113">PARAMETERS</span></span>

### <span data-ttu-id="ddca1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddca1-114">-DefaultProfile</span></span>
<span data-ttu-id="ddca1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddca1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddca1-116">-Включено</span><span class="sxs-lookup"><span data-stu-id="ddca1-116">-Enabled</span></span>
<span data-ttu-id="ddca1-117">Включает параметр.</span><span class="sxs-lookup"><span data-stu-id="ddca1-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddca1-118">-InputObject</span></span>
<span data-ttu-id="ddca1-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="ddca1-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddca1-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="ddca1-120">-SettingKind</span></span>
<span data-ttu-id="ddca1-121">Тип параметра.</span><span class="sxs-lookup"><span data-stu-id="ddca1-121">Setting kind.</span></span> <span data-ttu-id="ddca1-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="ddca1-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca1-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ddca1-123">-SettingName</span></span>
<span data-ttu-id="ddca1-124">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="ddca1-124">Setting name.</span></span> <span data-ttu-id="ddca1-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="ddca1-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddca1-126">-Confirm</span></span>
<span data-ttu-id="ddca1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddca1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddca1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddca1-128">-WhatIf</span></span>
<span data-ttu-id="ddca1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddca1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddca1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddca1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddca1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddca1-131">CommonParameters</span></span>
<span data-ttu-id="ddca1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddca1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddca1-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddca1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddca1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddca1-134">INPUTS</span></span>

### <span data-ttu-id="ddca1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ddca1-135">System.String</span></span>
### <span data-ttu-id="ddca1-136">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ddca1-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="ddca1-137">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="ddca1-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="ddca1-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddca1-138">System.Boolean</span></span>

## <span data-ttu-id="ddca1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddca1-139">OUTPUTS</span></span>

### <span data-ttu-id="ddca1-140">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ddca1-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="ddca1-141">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="ddca1-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="ddca1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddca1-142">NOTES</span></span>

## <span data-ttu-id="ddca1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddca1-143">RELATED LINKS</span></span>
