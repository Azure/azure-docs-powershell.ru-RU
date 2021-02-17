---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240269"
---
# <span data-ttu-id="9938a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9938a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="9938a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9938a-102">SYNOPSIS</span></span>
<span data-ttu-id="9938a-103">Удаляет указанное сопоставление контейнера "Защита от восстановления сайтов Azure".</span><span class="sxs-lookup"><span data-stu-id="9938a-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="9938a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9938a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9938a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9938a-105">DESCRIPTION</span></span>
<span data-ttu-id="9938a-106">С **его** использованием удаляется указанное сопоставление контейнера защиты от восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="9938a-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="9938a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9938a-107">EXAMPLES</span></span>

### <span data-ttu-id="9938a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9938a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="9938a-109">Начало удаления указанного сопоставления контейнера защиты и возврат задания asR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="9938a-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9938a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9938a-110">PARAMETERS</span></span>

### <span data-ttu-id="9938a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9938a-111">-DefaultProfile</span></span>
<span data-ttu-id="9938a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9938a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9938a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9938a-113">-Force</span></span>
<span data-ttu-id="9938a-114">Принудительно выполнить команду, не предоставляя дополнительное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="9938a-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9938a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9938a-115">-InputObject</span></span>
<span data-ttu-id="9938a-116">Объект ввода для cmdlet: объект сопоставления контейнера защиты ASR, соответствующий удаляемму контейнеру защиты.</span><span class="sxs-lookup"><span data-stu-id="9938a-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="9938a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9938a-117">-Confirm</span></span>
<span data-ttu-id="9938a-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9938a-118">Specify if confirmation is required.</span></span> <span data-ttu-id="9938a-119">Установите для параметра подтверждения значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9938a-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="9938a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9938a-120">-WhatIf</span></span>
<span data-ttu-id="9938a-121">Показывает, что произойдет, если выполняется cmdlet без его выполнения.</span><span class="sxs-lookup"><span data-stu-id="9938a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9938a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9938a-122">CommonParameters</span></span>
<span data-ttu-id="9938a-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9938a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9938a-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9938a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9938a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9938a-125">INPUTS</span></span>

### <span data-ttu-id="9938a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9938a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="9938a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9938a-127">OUTPUTS</span></span>

### <span data-ttu-id="9938a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9938a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9938a-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9938a-129">NOTES</span></span>

## <span data-ttu-id="9938a-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9938a-130">RELATED LINKS</span></span>

[<span data-ttu-id="9938a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9938a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="9938a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9938a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
