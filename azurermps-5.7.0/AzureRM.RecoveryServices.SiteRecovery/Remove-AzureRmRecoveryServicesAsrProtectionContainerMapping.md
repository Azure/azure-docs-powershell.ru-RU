---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732846"
---
# <span data-ttu-id="72ce1-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="72ce1-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="72ce1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="72ce1-103">Удаляет указанное сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="72ce1-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ce1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72ce1-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ce1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72ce1-105">DESCRIPTION</span></span>
<span data-ttu-id="72ce1-106">Командлет **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** удаляет указанное сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="72ce1-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="72ce1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72ce1-107">EXAMPLES</span></span>

### <span data-ttu-id="72ce1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72ce1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="72ce1-109">Запускает удаление указанного сопоставления контейнера защиты и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="72ce1-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72ce1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72ce1-110">PARAMETERS</span></span>

### <span data-ttu-id="72ce1-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72ce1-111">-Confirm</span></span>
<span data-ttu-id="72ce1-112">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="72ce1-112">Specify if confirmation is required.</span></span> <span data-ttu-id="72ce1-113">Установка значения параметра Confirm в $false для пропуска подтверждения</span><span class="sxs-lookup"><span data-stu-id="72ce1-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ce1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ce1-114">-DefaultProfile</span></span>
<span data-ttu-id="72ce1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72ce1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ce1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="72ce1-116">-Force</span></span>
<span data-ttu-id="72ce1-117">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="72ce1-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ce1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72ce1-118">-InputObject</span></span>
<span data-ttu-id="72ce1-119">Входной объект для командлета: объект сопоставления контейнера защиты ASR, соответствующий удаляемому контейнеру защиты.</span><span class="sxs-lookup"><span data-stu-id="72ce1-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72ce1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ce1-120">-WhatIf</span></span>
<span data-ttu-id="72ce1-121">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="72ce1-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ce1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ce1-122">CommonParameters</span></span>
<span data-ttu-id="72ce1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72ce1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ce1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ce1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ce1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72ce1-125">INPUTS</span></span>

### <span data-ttu-id="72ce1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="72ce1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="72ce1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72ce1-127">OUTPUTS</span></span>

### <span data-ttu-id="72ce1-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="72ce1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72ce1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="72ce1-129">NOTES</span></span>

## <span data-ttu-id="72ce1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72ce1-130">RELATED LINKS</span></span>

[<span data-ttu-id="72ce1-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="72ce1-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="72ce1-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="72ce1-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
