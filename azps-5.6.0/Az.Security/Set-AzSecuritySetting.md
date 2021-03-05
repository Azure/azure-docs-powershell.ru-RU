---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 5c7e9d80ffd9109cda1f13f74b1febb3b28e10ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005747"
---
# <span data-ttu-id="2a780-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2a780-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="2a780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a780-102">SYNOPSIS</span></span>
<span data-ttu-id="2a780-103">Обновление параметров безопасности в Центре безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="2a780-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="2a780-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a780-104">SYNTAX</span></span>

### <span data-ttu-id="2a780-105">GeneralScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a780-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a780-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="2a780-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a780-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a780-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a780-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a780-108">DESCRIPTION</span></span>
<span data-ttu-id="2a780-109">Новый Set-AzSecuritySetting обновляет определенный параметр безопасности в Центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="2a780-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="2a780-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a780-110">EXAMPLES</span></span>

### <span data-ttu-id="2a780-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a780-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="2a780-112">Обновление параметра экспорта данных MCAS</span><span class="sxs-lookup"><span data-stu-id="2a780-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="2a780-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a780-113">PARAMETERS</span></span>

### <span data-ttu-id="2a780-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a780-114">-DefaultProfile</span></span>
<span data-ttu-id="2a780-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a780-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a780-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2a780-116">-Enabled</span></span>
<span data-ttu-id="2a780-117">Включает параметр.</span><span class="sxs-lookup"><span data-stu-id="2a780-117">Enables the setting.</span></span>

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

### <span data-ttu-id="2a780-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a780-118">-InputObject</span></span>
<span data-ttu-id="2a780-119">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="2a780-119">Input Object.</span></span>

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

### <span data-ttu-id="2a780-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="2a780-120">-SettingKind</span></span>
<span data-ttu-id="2a780-121">Тип параметра.</span><span class="sxs-lookup"><span data-stu-id="2a780-121">Setting kind.</span></span> <span data-ttu-id="2a780-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="2a780-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="2a780-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="2a780-123">-SettingName</span></span>
<span data-ttu-id="2a780-124">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="2a780-124">Setting name.</span></span> <span data-ttu-id="2a780-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="2a780-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="2a780-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a780-126">-Confirm</span></span>
<span data-ttu-id="2a780-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a780-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a780-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a780-128">-WhatIf</span></span>
<span data-ttu-id="2a780-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a780-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a780-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a780-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a780-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a780-131">CommonParameters</span></span>
<span data-ttu-id="2a780-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a780-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a780-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a780-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a780-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a780-134">INPUTS</span></span>

### <span data-ttu-id="2a780-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2a780-135">System.String</span></span>
### <span data-ttu-id="2a780-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2a780-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="2a780-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="2a780-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="2a780-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a780-138">System.Boolean</span></span>

## <span data-ttu-id="2a780-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a780-139">OUTPUTS</span></span>

### <span data-ttu-id="2a780-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2a780-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="2a780-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="2a780-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="2a780-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a780-142">NOTES</span></span>

## <span data-ttu-id="2a780-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a780-143">RELATED LINKS</span></span>
