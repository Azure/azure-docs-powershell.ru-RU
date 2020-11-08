---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246838"
---
# <span data-ttu-id="426e3-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="426e3-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="426e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="426e3-102">SYNOPSIS</span></span>
<span data-ttu-id="426e3-103">Обновите сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="426e3-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="426e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="426e3-104">SYNTAX</span></span>

### <span data-ttu-id="426e3-105">AzureToAzureEnableAutoUpdate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="426e3-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="426e3-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="426e3-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="426e3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="426e3-107">DESCRIPTION</span></span>
<span data-ttu-id="426e3-108">Командлет **Update-AzRecoveryServicesAsrProtectionContainerMapping** обновляет указанное сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="426e3-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="426e3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="426e3-109">EXAMPLES</span></span>

### <span data-ttu-id="426e3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="426e3-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="426e3-111">Запустите операцию, чтобы отключить автоматическое обновление для контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e3-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="426e3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="426e3-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="426e3-113">Запустите операцию, чтобы отключить функцию включения автоматического обновления для контейнера.</span><span class="sxs-lookup"><span data-stu-id="426e3-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="426e3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="426e3-114">PARAMETERS</span></span>

### <span data-ttu-id="426e3-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="426e3-115">-AutomationAccountId</span></span>
<span data-ttu-id="426e3-116">Указывает accountId автоматизации, используемую для автоматического UDPATE.</span><span class="sxs-lookup"><span data-stu-id="426e3-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="426e3-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="426e3-117">-AzureToAzure</span></span>
<span data-ttu-id="426e3-118">Указывает контейнер защиты Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="426e3-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="426e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426e3-119">-DefaultProfile</span></span>
<span data-ttu-id="426e3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="426e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="426e3-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="426e3-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="426e3-122">Параметр Switch, чтобы отключить автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="426e3-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="426e3-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="426e3-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="426e3-124">Параметр Switch, чтобы включить автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="426e3-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="426e3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="426e3-125">-InputObject</span></span>
<span data-ttu-id="426e3-126">Объект для сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="426e3-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="426e3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="426e3-127">-Confirm</span></span>
<span data-ttu-id="426e3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="426e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426e3-129">-WhatIf</span></span>
<span data-ttu-id="426e3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="426e3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="426e3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="426e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="426e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426e3-132">CommonParameters</span></span>
<span data-ttu-id="426e3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="426e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426e3-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="426e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426e3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="426e3-135">INPUTS</span></span>

### <span data-ttu-id="426e3-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="426e3-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="426e3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="426e3-137">OUTPUTS</span></span>

### <span data-ttu-id="426e3-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="426e3-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="426e3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="426e3-139">NOTES</span></span>

## <span data-ttu-id="426e3-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="426e3-140">RELATED LINKS</span></span>
