---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 29c996036705e3fc71f1c6a04ead16c24b1b3bca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951000"
---
# <span data-ttu-id="fe587-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fe587-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="fe587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe587-102">SYNOPSIS</span></span>
<span data-ttu-id="fe587-103">Обновите сопоставление контейнера для защиты от восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="fe587-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="fe587-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe587-104">SYNTAX</span></span>

### <span data-ttu-id="fe587-105">AzureToAzureEnableAutoUpdate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe587-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe587-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="fe587-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe587-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe587-107">DESCRIPTION</span></span>
<span data-ttu-id="fe587-108">Для указанного сопоставления контейнера защиты от восстановления сайтов Azure обновляется проектлет **Update-AzRecoveryServicesAsrProtectionContainerMapping.**</span><span class="sxs-lookup"><span data-stu-id="fe587-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="fe587-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe587-109">EXAMPLES</span></span>

### <span data-ttu-id="fe587-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe587-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="fe587-111">Начните операцию, чтобы отключить автоматическое обновление контейнера.</span><span class="sxs-lookup"><span data-stu-id="fe587-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="fe587-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe587-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="fe587-113">Начните операцию, чтобы отключить автоматическое обновление контейнера.</span><span class="sxs-lookup"><span data-stu-id="fe587-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="fe587-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe587-114">PARAMETERS</span></span>

### <span data-ttu-id="fe587-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="fe587-115">-AutomationAccountId</span></span>
<span data-ttu-id="fe587-116">Определяет учетную запись автоматизации, используемую для автоматического udpate.</span><span class="sxs-lookup"><span data-stu-id="fe587-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe587-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="fe587-117">-AzureToAzure</span></span>
<span data-ttu-id="fe587-118">Указывает контейнер защиты Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="fe587-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe587-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe587-119">-DefaultProfile</span></span>
<span data-ttu-id="fe587-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe587-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe587-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="fe587-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="fe587-122">Переключение параметра для отключения автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="fe587-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe587-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="fe587-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="fe587-124">Переключить параметр, чтобы включить автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="fe587-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe587-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe587-125">-InputObject</span></span>
<span data-ttu-id="fe587-126">Объект для сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="fe587-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe587-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe587-127">-Confirm</span></span>
<span data-ttu-id="fe587-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe587-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe587-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe587-129">-WhatIf</span></span>
<span data-ttu-id="fe587-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe587-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe587-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe587-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe587-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe587-132">CommonParameters</span></span>
<span data-ttu-id="fe587-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe587-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe587-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe587-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe587-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe587-135">INPUTS</span></span>

### <span data-ttu-id="fe587-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fe587-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="fe587-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe587-137">OUTPUTS</span></span>

### <span data-ttu-id="fe587-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fe587-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fe587-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe587-139">NOTES</span></span>

## <span data-ttu-id="fe587-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe587-140">RELATED LINKS</span></span>
