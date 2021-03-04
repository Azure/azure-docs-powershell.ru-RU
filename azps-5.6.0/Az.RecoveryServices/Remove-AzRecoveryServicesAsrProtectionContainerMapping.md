---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953251"
---
# <span data-ttu-id="49c50-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49c50-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="49c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c50-102">SYNOPSIS</span></span>
<span data-ttu-id="49c50-103">Удаляет указанное сопоставление контейнера "Защита от восстановления сайтов Azure".</span><span class="sxs-lookup"><span data-stu-id="49c50-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="49c50-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49c50-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c50-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c50-105">DESCRIPTION</span></span>
<span data-ttu-id="49c50-106">С **его** использованием удаляется указанное сопоставление контейнера защиты от восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="49c50-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="49c50-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49c50-107">EXAMPLES</span></span>

### <span data-ttu-id="49c50-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49c50-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="49c50-109">Начало удаления указанного сопоставления контейнера защиты и возврат задания asR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="49c50-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="49c50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c50-110">PARAMETERS</span></span>

### <span data-ttu-id="49c50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c50-111">-DefaultProfile</span></span>
<span data-ttu-id="49c50-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49c50-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="49c50-113">-Force</span><span class="sxs-lookup"><span data-stu-id="49c50-113">-Force</span></span>
<span data-ttu-id="49c50-114">Принудительно выполнить команду, не предоставляя дополнительное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="49c50-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="49c50-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49c50-115">-InputObject</span></span>
<span data-ttu-id="49c50-116">Объект ввода для cmdlet: объект сопоставления контейнера защиты ASR, соответствующий удаляемму контейнеру защиты.</span><span class="sxs-lookup"><span data-stu-id="49c50-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="49c50-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49c50-117">-Confirm</span></span>
<span data-ttu-id="49c50-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="49c50-118">Specify if confirmation is required.</span></span> <span data-ttu-id="49c50-119">Установите для параметра подтверждения значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="49c50-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="49c50-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c50-120">-WhatIf</span></span>
<span data-ttu-id="49c50-121">Показывает, что произойдет, если выполняется cmdlet без его выполнения.</span><span class="sxs-lookup"><span data-stu-id="49c50-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="49c50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c50-122">CommonParameters</span></span>
<span data-ttu-id="49c50-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c50-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c50-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c50-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49c50-125">INPUTS</span></span>

### <span data-ttu-id="49c50-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49c50-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="49c50-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49c50-127">OUTPUTS</span></span>

### <span data-ttu-id="49c50-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="49c50-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="49c50-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49c50-129">NOTES</span></span>

## <span data-ttu-id="49c50-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49c50-130">RELATED LINKS</span></span>

[<span data-ttu-id="49c50-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49c50-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="49c50-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="49c50-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
