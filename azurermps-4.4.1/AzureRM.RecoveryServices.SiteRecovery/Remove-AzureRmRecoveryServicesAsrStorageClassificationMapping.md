---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567543"
---
# <span data-ttu-id="5435b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5435b-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="5435b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5435b-102">SYNOPSIS</span></span>
<span data-ttu-id="5435b-103">Удаляет указанное сопоставление классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="5435b-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5435b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5435b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5435b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5435b-105">DESCRIPTION</span></span>
<span data-ttu-id="5435b-106">Командлет **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** удаляет указанное сопоставление классификации хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5435b-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="5435b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5435b-107">EXAMPLES</span></span>

### <span data-ttu-id="5435b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5435b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="5435b-109">Запускает удаление указанного сопоставления классификации хранилища и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="5435b-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5435b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5435b-110">PARAMETERS</span></span>

### <span data-ttu-id="5435b-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5435b-111">-InputObject</span></span>
<span data-ttu-id="5435b-112">Входной объект для командлета: объект сопоставления классификации хранилища ASR, соответствующий сопоставлению классификации хранилища ASR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5435b-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5435b-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5435b-113">-Confirm</span></span>
<span data-ttu-id="5435b-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5435b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5435b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5435b-115">-WhatIf</span></span>
<span data-ttu-id="5435b-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5435b-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5435b-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5435b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5435b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5435b-118">CommonParameters</span></span>
<span data-ttu-id="5435b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5435b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5435b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5435b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5435b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5435b-121">INPUTS</span></span>

### <span data-ttu-id="5435b-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5435b-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="5435b-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5435b-123">OUTPUTS</span></span>

### <span data-ttu-id="5435b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5435b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5435b-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5435b-125">NOTES</span></span>

## <span data-ttu-id="5435b-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5435b-126">RELATED LINKS</span></span>

[<span data-ttu-id="5435b-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5435b-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="5435b-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5435b-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
