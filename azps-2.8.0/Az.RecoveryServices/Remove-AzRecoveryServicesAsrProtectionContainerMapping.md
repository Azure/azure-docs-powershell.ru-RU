---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 9ff992231e48efdfa9873aae75fc602ccd53a64e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905845"
---
# <span data-ttu-id="7900b-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7900b-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="7900b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7900b-102">SYNOPSIS</span></span>
<span data-ttu-id="7900b-103">Удаляет указанное сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7900b-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="7900b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7900b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7900b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7900b-105">DESCRIPTION</span></span>
<span data-ttu-id="7900b-106">Командлет **Remove-AzRecoveryServicesAsrProtectionContainerMapping** удаляет указанное сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7900b-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="7900b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7900b-107">EXAMPLES</span></span>

### <span data-ttu-id="7900b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7900b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7900b-109">Запускает удаление указанного сопоставления контейнера защиты и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="7900b-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7900b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7900b-110">PARAMETERS</span></span>

### <span data-ttu-id="7900b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7900b-111">-DefaultProfile</span></span>
<span data-ttu-id="7900b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7900b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7900b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7900b-113">-Force</span></span>
<span data-ttu-id="7900b-114">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="7900b-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="7900b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7900b-115">-InputObject</span></span>
<span data-ttu-id="7900b-116">Входной объект для командлета: объект сопоставления контейнера защиты ASR, соответствующий удаляемому контейнеру защиты.</span><span class="sxs-lookup"><span data-stu-id="7900b-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="7900b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7900b-117">-Confirm</span></span>
<span data-ttu-id="7900b-118">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7900b-118">Specify if confirmation is required.</span></span> <span data-ttu-id="7900b-119">Установка значения параметра Confirm в $false для пропуска подтверждения</span><span class="sxs-lookup"><span data-stu-id="7900b-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="7900b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7900b-120">-WhatIf</span></span>
<span data-ttu-id="7900b-121">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="7900b-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7900b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7900b-122">CommonParameters</span></span>
<span data-ttu-id="7900b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7900b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7900b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7900b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7900b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7900b-125">INPUTS</span></span>

### <span data-ttu-id="7900b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7900b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="7900b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7900b-127">OUTPUTS</span></span>

### <span data-ttu-id="7900b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7900b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7900b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7900b-129">NOTES</span></span>

## <span data-ttu-id="7900b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7900b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7900b-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7900b-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="7900b-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7900b-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
